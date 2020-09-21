---
title: Escreva e simule programas de nível qubit no Q#
description: Tutorial passo a passo sobre como escrever e simular um programa Quantum que opera no nível de qubit individual
author: gillenhaalb
ms.author: a-gibec
ms.date: 10/06/2019
uid: microsoft.quantum.circuit-tutorial
ms.topic: tutorial
no-loc:
- Q#
- $$v
ms.openlocfilehash: 0dbeee8e092c830576ba8f79733035cdeeac11de
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834951"
---
# <a name="tutorial-write-and-simulate-qubit-level-programs-in-q"></a>Tutorial: escrever e simular programas de nível qubit em Q\#

Bem-vindo ao tutorial do kit de desenvolvimento do Quantum sobre como escrever e simular um programa Quantum básico que opera em qubits individuais. 

Embora o Q# tenha sido criado principalmente como uma linguagem de programação de alto nível para programas Quantum de grande escala, ele pode ser facilmente usado para explorar o nível inferior dos programas Quantum: endereçando diretamente qubits específico.
A flexibilidade do Q# permite aos usuários abordar sistemas Quantum a partir de qualquer nível de abstração, e neste tutorial vamos nos aprofundar no próprio qubits.
Especificamente, examinamos os bastidores da [transformação de Fourier do Quantum](https://en.wikipedia.org/wiki/Quantum_Fourier_transform), uma sub-rotina que é integral para muitos algoritmos maiores do Quantum.

Observe que essa exibição de nível baixo do processamento de informações Quantum geralmente é descrita em termos de "[circuitos Quantum](xref:microsoft.quantum.concepts.circuits)", que representam a aplicação sequencial de Gates a qubits específicas de um sistema.

Assim, as operações únicas e qubit que aplicamos sequencialmente podem ser prontamente representadas em um "diagrama de circuito".
Em nosso caso, definiremos uma Q# operação para executar a transformação de Fourier do quantum de três qubit completa, que tem a seguinte representação como um circuito:

<br/>
<img src="../media/qft_full.PNG" alt="Three qubit quantum Fourier transform circuit diagram" width="600">

## <a name="prerequisites"></a>Pré-requisitos

* [Instale](xref:microsoft.quantum.install) o kit de desenvolvimento Quantum usando o ambiente de desenvolvimento e a linguagem preferencial.
* Caso já tenha o QDK instalado, verifique se você o [atualizou](xref:microsoft.quantum.update) para a última versão


## <a name="in-this-tutorial-youll-learn-how-to"></a>Neste tutorial, você aprenderá como:

> [!div class="checklist"]
> * Definir operações Quantum no Q#
> * Chamar Q# operações diretamente do prompt de comando ou usando um programa de host clássico
> * Simular uma operação Quantum de alocação qubit para saída de medida
> * Observe como o wavefunction simulado do sistema Quantum evolui em toda a operação

A execução de um programa Quantum com o kit de desenvolvimento Quantum da Microsoft normalmente consiste em duas partes:
1. O próprio programa, que é implementado usando a Q# linguagem de programação Quantum e, em seguida, invocado para ser executado em um computador Quantum ou simulador Quantum. Consistem em 
    - Q# operações: sub-rotinas que atuam em registros de Quantum e 
    - Q# funções: sub-rotinas clássicas usadas dentro do algoritmo Quantum.
2. O ponto de entrada usado para chamar o programa Quantum e especificar o computador de destino no qual ele deve ser executado.
    Isso pode ser feito diretamente do prompt de comando ou por meio de um programa de host escrito em uma linguagem de programação clássica, como Python ou C#.
    Este tutorial inclui instruções para qualquer método que você preferir.

## <a name="allocate-qubits-and-define-quantum-operations"></a>Alocar qubits e definir operações Quantum

A primeira parte deste tutorial consiste em definir a Q# operação `Perform3qubitQFT` , que executa a transformação de Fourier do Quantum em três qubits. 

Além disso, usaremos a [`DumpMachine`](xref:microsoft.quantum.diagnostics.dumpmachine) função para observar como o wavefunction simulado de nosso sistema de três qubit evolui na operação.

A primeira etapa é criar seu Q# projeto e arquivo.
As etapas para isso dependem do ambiente que você usará para chamar o programa e pode encontrar os detalhes nos respectivos [guias de instalação](xref:microsoft.quantum.install).

Descreveremos os componentes do arquivo passo a passo, mas o código também está disponível como um bloco completo abaixo.

### <a name="namespaces-to-access-other-no-locq-operations"></a>Namespaces para acessar outras Q# operações
Dentro do arquivo, primeiro definimos o namespace `NamespaceQFT` que será acessado pelo compilador.
Para que nossa operação faça uso de Q# operações existentes, abrimos os `Microsoft.Quantum.<>` namespaces relevantes.

```qsharp
namespace NamespaceQFT {
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;
    open Microsoft.Quantum.Math;
    open Microsoft.Quantum.Arrays;

    // operations go here
}
```

### <a name="define-operations-with-arguments-and-returns"></a>Definir operações com argumentos e Devoluções
Em seguida, definimos a `Perform3qubitQFT` operação:

```qsharp
    operation Perform3qubitQFT() : Unit {
        // do stuff
    }
```

Por enquanto, a operação não usa argumentos e não retorna nada---, nesse caso, escrevemos que ele retorna um `Unit` objeto, que é semelhante a `void` em C# ou uma tupla vazia, `Tuple[()]` em Python.
Posteriormente, iremos modificá-lo para retornar uma matriz de resultados de medição, em que ponto `Unit` será substituído por `Result[]` . 

### <a name="allocate-qubits-with-using"></a>Alocar qubits com `using`
Em nossa Q# operação, primeiro alocamos um registro de três qubits com a `using` instrução:

```qsharp
        using (qs = Qubit[3]) {

            Message("Initial state |000>:");
            DumpMachine();

        }
```

Com `using` o, os qubits são alocados automaticamente no estado $ \ket {0} $. Podemos verificar isso usando [`Message(<string>)`](xref:microsoft.quantum.intrinsic.message) e [`DumpMachine()`](xref:microsoft.quantum.diagnostics.dumpmachine) , que imprime uma cadeia de caracteres e o estado atual do sistema para o console.

> [!NOTE]
> As `Message(<string>)` `DumpMachine()` funções e (de [`Microsoft.Quantum.Intrinsic`](xref:microsoft.quantum.intrinsic) e [`Microsoft.Quantum.Diagnostics`](xref:microsoft.quantum.diagnostics) , respectivamente) são impressas diretamente no console. Assim como uma computação Quantum real, Q# o não nos permite acessar diretamente os Estados de qubit.
> No entanto, como `DumpMachine` imprime o estado atual do computador de destino, ele pode fornecer Insight valioso para depuração e aprendizagem quando usado em conjunto com o simulador de estado completo.


### <a name="applying-single-qubit-and-controlled-gates"></a>Aplicando Gates qubit e controlado

Em seguida, aplicamos as Gates que compõem a própria operação.
Q# já contém muitas Gates básicas de Quantum como operações no [`Microsoft.Quantum.Intrinsic`](xref:microsoft.quantum.intrinsic) namespace, e essas não são exceção. 

Dentro de uma Q# operação, as instruções que chamam o callablefiles, é claro, serão executadas em ordem sequencial.
Portanto, o primeiro portão a ser aplicado é o [`H`](xref:microsoft.quantum.intrinsic.h) (Hadamard) para o primeiro qubit:

<br/>
<img src="../media/qft_firstH.PNG" alt="Circuit diagram for three qubit QFT through first Hadamard" width="120">

Para aplicar uma operação a um qubit específico de um registro (ou seja, um único `Qubit` de uma matriz `Qubit[]` ), usamos a notação de índice padrão.
Portanto, aplicar o [`H`](xref:microsoft.quantum.intrinsic.h) à primeira qubit do nosso registro `qs` assume a forma:

```qsharp
            H(qs[0]);
```

Além de aplicar o `H` portão (Hadamard) a qubits individuais, o circuito QFT consiste principalmente em [`R1`](xref:microsoft.quantum.intrinsic.r1) rotações controladas.
Uma `R1(θ, <qubit>)` operação em geral deixa o componente $ \ket {0} $ do qubit inalterado, ao mesmo tempo em que aplica uma rotação de $e ^ {i\theta} $ ao componente $ \ket {1} $.

#### <a name="controlled-operations"></a>Operações controladas

Q# torna extremamente fácil a condição da execução de uma operação em um ou vários qubits de controle.
Em geral, simplesmente precedemos a chamada com `Controlled` e os argumentos da operação são alterados como:

 `Op(<normal args>)` $ \tO $ `Controlled Op([<control qubits>], (<normal args>))` .

Observe que o qubits de controle deve ser fornecido como uma matriz, mesmo se for um único qubit.

Após o `H` , vemos que as próximas Gates são as `R1` Gates que atuam na primeira qubit (e controladas pela segunda/terceira):

<br/>
<img src="../media/qft_firstqubit.PNG" alt="Circuit diagram for three qubit QFT through first qubit" width="310">

Chamamos isso de

```qsharp
            Controlled R1([qs[1]], (PI()/2.0, qs[0]));
            Controlled R1([qs[2]], (PI()/4.0, qs[0]));
```

Observe que usamos a [`PI()`](xref:microsoft.quantum.math.pi) função do [`Microsoft.Quantum.Math`](xref:microsoft.quantum.math) namespace para definir as rotações em termos de pi radianos.
Além disso, dividimos por um `Double` (por exemplo, `2.0` ) porque dividir por um inteiro `2` geraria um erro de tipo. 

> [!TIP]
> `R1(π/2)` e `R1(π/4)` são equivalentes às `S` `T` operações e (também em `Microsoft.Quantum.Intrinsic` ).


Depois de aplicar as `H` operações relevantes e as rotações controladas à segunda e terceira qubits:

```qsharp
            //second qubit:
            H(qs[1]);
            Controlled R1([qs[2]], (PI()/2.0, qs[1]));

            //third qubit:
            H(qs[2]);
```

Precisamos aplicar um portão apenas [`SWAP`](xref:microsoft.quantum.intrinsic.swap) para concluir o circuito:

```qsharp
            SWAP(qs[2], qs[0]);
```

Isso é necessário porque a natureza da transformação de Fourier do Quantum gera o qubits na ordem inversa, portanto, as trocas permitem a integração direta da sub-rotina em algoritmos maiores.

Portanto, terminamos de escrever as operações de nível qubit da transformação de Fourier do Quantum em nossa Q# operação:

<img src="../media/qft_full.PNG" alt="Three qubit quantum Fourier transform circuit diagram" width="600">

No entanto, não podemos chamá-lo um dia mesmo.
Nossos qubits estavam no estado $ \ket {0} $ quando os alocamos, e muito parecidos na vida, devemos Q# deixar coisas da mesma forma que as encontramos (ou melhor!).

### <a name="deallocate-qubits"></a>Desalocar qubits

Chamamos [`DumpMachine()`](xref:microsoft.quantum.diagnostics.dumpmachine) novamente para ver o estado de pós-operação e, por fim, aplicam [`ResetAll`](xref:microsoft.quantum.intrinsic.resetall) -se ao registro qubit para redefinir nosso qubits para $ \ket {0} $ antes de concluir a operação:

```qsharp
            Message("After:");
            DumpMachine();

            ResetAll(qs);
```

Exigir que todos os qubits desalocados sejam explicitamente definidos como $ \ket {0} $ é um recurso básico do Q# , pois permite que outras operações saibam seu estado precisamente quando começam a usar esses mesmos qubits (um recurso escasso).
Além disso, isso garante que eles não sejam confusas com nenhum outro qubits no sistema.
Se a redefinição não for executada no final de um `using` bloco de alocação, um erro de tempo de execução será gerado.

O Q# arquivo completo agora deve ser assim:

```qsharp
namespace NamespaceQFT {
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;
    open Microsoft.Quantum.Math;
    open Microsoft.Quantum.Arrays;

    operation Perform3qubitQFT() : Unit {

        using (qs = Qubit[3]) {

            Message("Initial state |000>:");
            DumpMachine();

            //QFT:
            //first qubit:
            H(qs[0]);
            Controlled R1([qs[1]], (PI()/2.0, qs[0]));
            Controlled R1([qs[2]], (PI()/4.0, qs[0]));

            //second qubit:
            H(qs[1]);
            Controlled R1([qs[2]], (PI()/2.0, qs[1]));

            //third qubit:
            H(qs[2]);

            SWAP(qs[2], qs[0]);

            Message("After:");
            DumpMachine();

            ResetAll(qs);
        }
    }
}
```


Com o Q# arquivo e a operação concluídos, nosso programa Quantum está pronto para ser chamado e simulado.

## <a name="run-the-program"></a>Execute o programa

Depois de definir nossa Q# operação em um `.qs` arquivo, agora precisamos chamar essa operação e observar os dados clássicos retornados.
Por enquanto, não há nada retornado (Lembre-se de que nossa operação definida acima retorna `Unit` ), mas quando modificamos posteriormente a Q# operação para retornar uma matriz de resultados de medida ( `Result[]` ), abordaremos isso.

Embora o Q# programa esteja onipresente em todos os ambientes usados para chamá-lo, a maneira de fazer isso é, certamente, diferente. Como tal, basta seguir as instruções na guia correspondente à sua configuração: trabalhando no Q# aplicativo ou usando um programa de host em Python ou C#.

#### <a name="command-prompt"></a>[Prompt de comando](#tab/tabid-cmdline)

A execução do Q# programa a partir do prompt de comando requer apenas uma pequena alteração no Q# arquivo.

Basta adicionar `@EntryPoint()` a uma linha anterior à definição da operação:

```qsharp
    @EntryPoint()
    operation Perform3qubitQFT() : Unit {
        // ...
```

Para executar o programa, abra o terminal na pasta do seu projeto e insira

```dotnetcli
dotnet run
```

Após a conclusão, você deverá ver `Message` as `DumpMachine` saídas e abaixo impressas em seu console.


#### <a name="python"></a>[Python](#tab/tabid-python)

Criar um arquivo de host do Python: `host.py` .

O arquivo de host é construído da seguinte maneira: 
1. Primeiro, importamos o `qsharp` módulo, que registra o carregador de módulo para Q# interoperabilidade. 
    Isso permite que Q# os namespaces (por exemplo `NamespaceQFT` , que definimos em nosso Q# arquivo) apareçam como módulos Python, do qual podemos importar Q# operações.
2. Em seguida, importe as Q# operações que invocaremos diretamente---nesse caso, `Perform3qubitQFT` .
    Precisamos importar apenas o ponto de entrada para um Q# programa (ou seja _not_ , operações como `H` e `R1` , que são chamadas por outras Q# operações, mas nunca pelo host clássico).
3. Ao simular Q# operações ou funções, use o formulário `<Q#callable>.simulate(<args>)` para executá-las no `QuantumSimulator()` computador de destino. 

> [!NOTE]
> Se quiséssemos chamar a operação em um computador diferente, por exemplo, o `ResourceEstimator()` , seria simplesmente usado `<Q#callable>.estimate_resources(<args>)` .
> Em geral, Q# as operações são independentes para os computadores nos quais elas são executadas, mas alguns recursos como `DumpMachine` podem se comportar de forma diferente.

4. Após a execução da simulação, a chamada de operação retornará valores conforme definido no Q# arquivo.
    Por enquanto, não há nada retornado, mas posteriormente, veremos um exemplo de atribuição e processamento desses valores.
    Com os dados resultantes em nossas mãos e totalmente clássicos, podemos fazer tudo o que gostaríamos com ele.

O `host.py` arquivo completo deve ser o seguinte:

```python
import qsharp
from NamespaceQFT import Perform3qubitQFT

Perform3qubitQFT.simulate()
```

Execute o arquivo Python e, em seu console, você verá as `Message` saídas e `DumpMachine` abaixo. 


#### <a name="c"></a>[C#](#tab/tabid-csharp)

Seguindo as mesmas instruções do guia de [instalação](xref:microsoft.quantum.install.cs)do, crie um arquivo de host C# e renomeie-o como `host.cs` .

O host C# tem quatro partes:
1. Constrói um simulador quântico.
    No código abaixo, essa é a variável `qsim` .
2. Calcula os argumentos necessários para o algoritmo quântico.
    Não há nenhum neste exemplo.
3. Executa o algoritmo quântico. 
    Cada Q# operação gera uma classe C# com o mesmo nome. 
    Essa classe tem um `Run` método que executa a operação de **forma assíncrona**.
    A execução é assíncrona porque executá-la no hardware real será assíncrona. 
    Como o `Run` método é assíncrono, chamamos o `Wait()` método; isso bloqueia a execução até que a tarefa seja concluída e retorna o resultado de forma síncrona. 
4. Processar o resultado retornado da operação.
    Por enquanto, a operação não retorna nada.


```csharp
using System;

using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace NamespaceQFT
{
    class Driver
    {
        static void Main(string[] args)
        {
            using (var qsim = new QuantumSimulator())
            {
                Perform3QubitQFT.Run(qsim).Wait();
            }
            
            System.Console.WriteLine("Press any key to continue...");
            Console.ReadKey();
        }
    }
}

```
Execute o aplicativo e a saída deve corresponder à seguinte.
O programa será encerrado depois que você pressionar uma tecla.
***

```Output
Initial state |000>:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|3>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
After:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
```

Quando chamado no simulador de estado completo, `DumpMachine()` fornece essas representações de vários do wavefunction do estado do Quantum. Os possíveis estados de um sistema $n $-qubit podem ser representados por Estados de base computacional $2 ^ n $, cada um com um coeficiente complexo correspondente (simplesmente uma amplitude e uma fase).
Os Estados de base computacional correspondem a todas as possíveis cadeias de caracteres binárias de comprimento $n $---ou seja, todas as combinações possíveis de Estados qubit $ \ket {0} $ e $ \ket {1} $, em que cada dígito binário corresponde a um qubit individual.

A primeira linha fornece um comentário com as IDs do qubits correspondente em sua ordem significativa.
Qubit `2` ser o "mais significativo" significa simplesmente que na representação binária do vetor de estado base $ \ket{i} $, o estado de qubit `2` corresponde ao dígito mais à esquerda. Por exemplo, $ \ket {6} = \ket {110} $ compreende qubits `2` e `1` ambos em $ \ket {1} $ e qubit `0` em $ \ket {0} $.


O restante das linhas descreve a amplitude de probabilidade de medir o vetor de estado base $ \ket{i} $ nos formatos cartesianas e polar.
Em detalhes para a primeira linha do nosso estado de entrada $ \ket {000} $:
* **`|0>:`** Essa linha corresponde ao `0` estado de base computacional (Considerando que nossa pós-alocação de estado inicial era $ \ket {000} $, esperamos que esse seja o único estado com amplitude de probabilidade neste ponto).
* **`1.000000 +  0.000000 i`**: a amplitude de probabilidade no formato cartesiano.
* **` == `**: o `equal` sinal separa as representações equivalentes.
* **`********************`**: Uma representação gráfica da magnitude, o número de `*` é proporcional à probabilidade de medir esse vetor de estado. 
* **`[ 1.000000 ]`**: o valor numérico da magnitude
* **`    ---`**: Uma representação gráfica da fase de amplitude.
* **`[ 0.0000 rad ]`**: o valor numérico da fase (em radianos).

A magnitude e a fase são exibidas com uma representação gráfica. A representação de magnitude é simples: ela mostra uma barra de `*` e quanto maior a probabilidade, maior será a barra. Para a fase, consulte [testando e Depurando: despejar funções](xref:microsoft.quantum.guide.testingdebugging#dump-functions) para as possíveis representações de símbolo com base em intervalos de ângulo.


Portanto, a saída impressa está ilustrando que nossas Gates programadas transformaram nosso estado de

$ $ \ket{\psi} \_ {Initial} = \ket {000} $ $

como 

$ $ \begin{align} \ket{\psi} \_ {final} &= \frac {1} {\sqrt {8} } \left (\ket {000} + \ket {001} + \ket {010} + \ket {011} + \ket {100} + \ket {101} + \ket {110} + \ket {111} \right) \\ \\ &= \frac {1} {\sqrt{2 ^ n}} \sum \_ {j = 0} ^ {2 ^ n-1} \ket{j}, \end{align} $ $

que é precisamente o comportamento da transformação de Fourier de 3 qubit. 

Se você estiver curioso sobre como outros Estados de entrada são afetados, incentivamos você a brincar com a aplicação de operações qubit antes da transformação.

## <a name="adding-measurements"></a>Adicionando medidas

Infelizmente, uma base da mecânica quantum nos informa que um sistema Quantum real não pode ter tal `DumpMachine` função. Em vez disso, somos forçados a extrair informações por meio de medidas, o que, em geral, não apenas consegue nos fornecer o estado completo do Quantum, mas também pode alterar drasticamente o próprio sistema.
Há muitos tipos de medidas de Quantum, mas nos concentraremos nas medidas mais básicas: projetadas em qubits único.
Na medida em uma determinada base (por exemplo, a base computacional $ \{ \ket {0} , \ket {1} \} $), o estado de qubit é projetado para qualquer estado base que foi medido---, portanto, destruir qualquer superposição entre os dois.

Para implementar medidas dentro de um Q# programa, usamos a `M` operação (from `Microsoft.Quantum.Intrinsic` ), que retorna um `Result` tipo.

Primeiro, modificamos nossa `Perform3QubitQFT` operação para retornar uma matriz de resultados de medição, `Result[]` em vez de `Unit` .

```qsharp
    operation Perform3QubitQFT() : Result[] {
```

#### <a name="define-and-initialize-result-array"></a>Definir e inicializar `Result[]` matriz

Antes de alocar qubits (ou seja, antes da `using` instrução), declaramos e ligamos essa matriz de comprimento 3 (uma `Result` para cada qubit): 

```qsharp
        mutable resultArray = new Result[3];
```

A `mutable` palavra-chave Preface `resultArray` permite que a variável seja reassociada posteriormente no código---por exemplo, ao adicionar nossos resultados de medição.

#### <a name="perform-measurements-in-a-for-loop-and-add-results-to-array"></a>Executar medidas em um `for` loop e adicionar resultados à matriz

Após as operações de transformação de Fourier dentro do `using` bloco, insira o seguinte código:

```qsharp
            for(i in IndexRange(qs)) {
                set resultArray w/= i <- M(qs[i]);
            }
```
A [`IndexRange`](xref:microsoft.quantum.arrays.indexrange) função chamada em uma matriz (por exemplo, nossa matriz de qubits `qs` ) retorna um intervalo sobre os índices da matriz. Aqui, usamos-o em nosso `for` loop para medir sequencialmente cada qubit usando a `M(qs[i])` instrução.
Cada tipo medido `Result` ( `Zero` ou `One` ) é então adicionado à posição de índice correspondente em `resultArray` com uma instrução UPDATE-and-REASSIGN.

> [!NOTE]
> A sintaxe dessa instrução é exclusiva para Q# , mas corresponde à reatribuição de variável semelhante `resultArray[i] <- M(qs[i])` vista em outras linguagens, como F # e R.

A palavra-chave `set` é sempre usada para reatribuir variáveis vinculadas usando `mutable` .

#### <a name="return-resultarray"></a>Exibir `resultArray`

Com todos os três qubits medidos e os resultados adicionados ao `resultArray` , somos seguros para redefinir e desalocar os qubits como antes.
Após o `using` fechamento do bloco, insira

```qsharp
        return resultArray;
```
para retornar, por fim, a saída de nossa operação. 

### <a name="understanding-the-effects-of-measurement"></a>Compreendendo os efeitos da medição

Vamos alterar o posicionamento de nossas `DumpMachine` funções para gerar o estado antes e depois das medições.
O código final da operação deve ser semelhante a: 

```qsharp
    operation Perform3QubitQFT() : Result[] {

        mutable resultArray = new Result[3];

        using (qs = Qubit[3]) {

            //QFT:
            //first qubit:
            H(qs[0]);
            Controlled R1([qs[1]], (PI()/2.0, qs[0]));
            Controlled R1([qs[2]], (PI()/4.0, qs[0]));

            //second qubit:
            H(qs[1]);
            Controlled R1([qs[2]], (PI()/2.0, qs[1]));

            //third qubit:
            H(qs[2]);

            SWAP(qs[2], qs[0]);

            Message("Before measurement: ");
            DumpMachine();

            for(i in IndexRange(qs)) {
                set resultArray w/= i <- M(qs[i]);
            }

            Message("After measurement: ");
            DumpMachine();

            ResetAll(qs);
        }
        return resultArray;
    }
}
```

Se você estiver trabalhando no prompt de comando, a matriz retornada será simplesmente exibida diretamente para o console no final da execução.
Caso contrário, atualize o programa de host para processar a matriz retornada.

#### <a name="command-prompt"></a>[Prompt de comando](#tab/tabid-cmdline)

Para ter mais conhecimento da matriz retornada que será impressa no console, podemos adicionar outro `Message` no Q# arquivo antes da `return` instrução:

```qsharp
        Message("Post-QFT measurement results [qubit0, qubit1, qubit2]: ");
        return resultArray;
```

Execute o projeto e a saída deverá ser semelhante ao seguinte:

```Output
Before measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
After measurement:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|3>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]

Post-QFT measurement results [qubit0, qubit1, qubit2]: 
[One,One,Zero]
```

#### <a name="python"></a>[Python](#tab/tabid-python)

Atualize seu programa Python para o seguinte:

```python
import qsharp
from NamespaceQFT import Perform3QubitQFT

measurementResult = Perform3QubitQFT.simulate()
print("\n")
print("Measured post-QFT state: [qubit0, qubit1, qubit2]")
print(measurementResult)

# reversing order to show corresponding basis state in binary form
binaryCompBasisState = ""
for i in measurementResult:
    binaryCompBasisState = str(i) + binaryCompBasisState
print("Corresponding basis state in binary:")
print("|" + binaryCompBasisState + ">")
```

Execute o arquivo e a saída deverá ser semelhante ao seguinte:

```Output
Before measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
After measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|3>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   

Post-QFT measurement results [qubit0, qubit1, qubit2]: 
[1, 1, 0]

Corresponding basis state in binary:
|011>
```

#### <a name="c"></a>[C#](#tab/tabid-csharp)

Agora que nossa operação está retornando um resultado, substitua a chamada de método `Wait()` pela busca da `Result` propriedade. Isso ainda realiza o mesmo Synchronicity discutido anteriormente, e podemos associar diretamente esse valor à variável `measurementResult` .

```csharp
using System;

using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace NamespaceQFT
{
    class Driver
    {
        static void Main(string[] args)
        {
            using (var qsim = new QuantumSimulator())
            {
                var measurementResult = Perform3QubitQFT.Run(qsim).Result;
                System.Console.WriteLine(
                    $"Post-QFT measurement results [qubit0, qubit1, qubit2]: ");
                System.Console.WriteLine(
                    measurementResult);

                // reversing order to show corresponding basis state in binary form
                string binaryCompBasisState = String.Empty;

                foreach (Result i in measurementResult)
                {
                    string iString = i.ToString();
                    binaryCompBasisState = iString + binaryCompBasisState;
                }
                binaryCompBasisState = "|" + binaryCompBasisState + ">";
                System.Console.WriteLine(
                    $"Corresponding basis state in binary:");
                System.Console.WriteLine(
                    binaryCompBasisState);
            }
            
            System.Console.WriteLine("Press any key to continue...");
            Console.ReadKey();
        }
    }
}
```

Execute o projeto e a saída deverá ser semelhante ao seguinte:

```Output
Before measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
After measurement:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|3>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]

Post-QFT measurement results [qubit0, qubit1, qubit2]: 
[One,One,Zero]

Corresponding basis state in binary:
|ZeroOneOne>

Press any key to continue...
```
***

Essa saída ilustra algumas coisas diferentes:
1. Comparando o resultado retornado à medida anterior `DumpMachine` , ele não ilustra _not_ a superposição QFT em relação a Estados de base.
    Uma medida retorna apenas um único estado de base, com uma probabilidade determinada pela amplitude desse Estado no wavefunction do sistema.
2. Da pós-medição `DumpMachine` , vemos que a medição _altera_ o estado em si, projetando-a da superposição inicial em relação a Estados de base única para o estado de base único que corresponde ao valor medido.

Se tivéssemos de repetir essa operação muitas vezes, veremos que as estatísticas de resultado começam a ilustrar a superposição ponderada igualmente do estado de QFT que dá ao aumento um resultado aleatório em cada imagem.
_No entanto_, além de serem ineficientes e ainda imperfeitos, isso só reproduziria as amplitudes relativas dos Estados de base, e não as fases relativas entre elas.
O último não é um problema neste exemplo, mas vemos que as fases relativas aparecem se uma entrada mais complexa fosse fornecida ao QFT do que $ \ket {000} $.

#### <a name="partial-measurements"></a>Medidas parciais 
Para explorar como medir apenas algumas qubits do registro pode afetar o estado do sistema, tente adicionar o seguinte dentro do `for` loop, após a linha de medida:
```qsharp
                let iString = IntAsString(i);
                Message("After measurement of qubit " + iString + ":");
                DumpMachine();
```

Observe que, para acessar a `IntAsString` função, você precisará adicionar 
```qsharp
    open Microsoft.Quantum.Convert;
```
com o restante das instruções de namespace `open` .

Na saída resultante, você verá a projeção gradual em subespaços, uma vez que cada qubit é medido.


## <a name="use-the-no-locq-libraries"></a>Usar as Q# bibliotecas
Como mencionamos na introdução, grande parte dos Q# restes de energia do fato de que ele permite abstrair as preocupações de lidar com qubits individuais.
Na verdade, se você quiser desenvolver programas Quantum que se aplicam em escala completa, se preocupar com o fato de que uma `H` operação vai antes ou depois de uma rotação específica apenas reduziria você. 

As Q# bibliotecas contêm a operação [QFT](xref:microsoft.quantum.canon.qft) , que você pode simplesmente tomar e aplicar para qualquer número de qubits.
Para experimentar, defina uma nova operação no Q# arquivo que tenha o mesmo conteúdo de `Perform3QubitQFT` , mas com tudo, desde o primeiro `H` até o `SWAP` substituído por duas linhas fáceis:
```qsharp
            let register = BigEndian(qs);    //from Microsoft.Quantum.Arithmetic
            QFT(register);                   //from Microsoft.Quantum.Canon
```
A primeira linha simplesmente cria uma [`BigEndian`](xref:microsoft.quantum.arithmetic.bigendian) expressão da matriz alocada de qubits, `qs` , que é o que a operação [QFT](xref:microsoft.quantum.canon.qft) utiliza como um argumento.
Isso corresponde à ordenação de índice do qubits no registro.

Para ter acesso a essas operações, adicione `open` instruções para seus respectivos namespaces no início do Q# arquivo:
```qsharp
    open Microsoft.Quantum.Canon;
    open Microsoft.Quantum.Arithmetic;
```

Agora, ajuste o programa de host para chamar o nome da nova operação (por exemplo `PerformIntrinsicQFT` ,) e dê a ele um experimente.

Para ver o verdadeiro benefício de usar as Q# operações de biblioteca, altere o número de qubits para algo diferente de `3` :
```qsharp
        mutable resultArray = new Result[4]; 

        using (qs = Qubit[4]) {
            //...
        }
```
Portanto, você pode aplicar o QFT apropriado para qualquer número determinado de qubits, sem precisar se preocupar com a bagunça de novas `H` operações e rotações em cada qubit.

Observe que o simulador Quantum leva exponencialmente mais tempo para ser executado à medida que você aumenta o número de qubits---precisamente por que estamos ansiosos para o hardware Quantum real!













