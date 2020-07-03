---
title: 'Maneiras de executar um programa Q #'
description: 'Visão geral das diferentes maneiras de executar os programas de Q #. Na linha de comando, p # Jupyter notebooks e programas de host clássico no Python ou em uma linguagem .NET.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 05/15/2020
ms.topic: article
uid: microsoft.quantum.guide.host-programs
ms.openlocfilehash: 132c138d7c392ed2b4bd3d0079180b68adae4cfc
ms.sourcegitcommit: a3775921db1dc5c653c97b8fa8fe2c0ddd5261ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/02/2020
ms.locfileid: "85887637"
---
# <a name="ways-to-run-a-q-program"></a>Maneiras de executar um programa Q #

Um dos maiores pontos fortes do kit de desenvolvimento Quantum é sua flexibilidade entre plataformas e ambientes de desenvolvimento.
No entanto, isso também significa que novos usuários do Q # podem se encontrar confusos ou sobrecarregados pelas inúmeras opções encontradas no [Guia de instalação](xref:microsoft.quantum.install).
Nesta página, explicaremos o que acontece quando um programa Q # é executado e comparamos as diferentes maneiras em que os usuários podem fazer isso.

Uma distinção principal é que Q # pode ser executada:
- como um aplicativo autônomo, em que Q # é o único idioma envolvido e o programa é invocado diretamente. Dois métodos realmente se enquadram nesta categoria:
  - a interface de linha de comando
  - Jupyter Notebooks do Q#
- com um *programa de host*adicional, escrito em Python ou em uma linguagem .net (por exemplo, C# ou F #), que invoca o programa e pode processar os resultados retornados.

Para entender melhor esses processos e suas diferenças, consideramos um programa simples de Q # e comparamos as maneiras como ele pode ser executado.

## <a name="basic-q-program"></a>Programa Basic Q #

Um programa Quantum básico pode consistir em preparar um qubit em uma superposição igual de Estados $ \ket {0} $ e $ \ket {1} $, medindo-o e retornando o resultado, que será aleatoriamente um desses dois Estados com probabilidade igual.
Na verdade, esse processo está no núcleo do início rápido do [gerador de números aleatórios Quantum](xref:microsoft.quantum.quickstarts.qrng) .

Em Q #, isso seria executado pelo seguinte código:

```qsharp
        using (q = Qubit()) {    // allocates qubit for use (automatically in |0>)
            H(q);                // puts qubit in superposition of |0> and |1>
            return MResetZ(q);   // measures qubit, returns result (and resets it to |0> before deallocation)
        }
```

No entanto, esse código sozinho não pode ser executado por Q #.
Para isso, ele precisa criar o corpo de uma [operação](xref:microsoft.quantum.guide.basics#q-operations-and-functions), que, em seguida, é executado quando chamado---diretamente ou por outra operação. Portanto, você pode escrever uma operação do seguinte formato:
```qsharp
    operation MeasureSuperposition() : Result {
        using (q = Qubit()) {
            H(q);
            return MResetZ(q);
        }
    }
```
Você definiu uma operação, `MeasureSuperposition` , que não recebe entradas e retorna um valor do tipo [Result](xref:microsoft.quantum.guide.types).

Embora os exemplos nesta página consistam apenas em *operações*q #, todos os conceitos que discutiremos referem-se igualmente às *funções*q # e, portanto, nos referimos a elas coletivamente como *chamáveis*. Suas diferenças são discutidas em [noções básicas de Q #: operações e funções](xref:microsoft.quantum.guide.basics#q-operations-and-functions)e mais detalhes sobre como defini-las podem ser encontradas em [operações e funções](xref:microsoft.quantum.guide.operationsfunctions).

### <a name="callable-defined-in-a-q-file"></a>Callable definido em um arquivo Q #

O callable é precisamente o que é chamado e executado por Q #.
No entanto, ele requer mais algumas adições para incluir um `*.qs` arquivo Q # completo.

Todos os tipos de Q # e os chamados (aqueles que você define e os intrínsecos ao idioma) são definidos em *namespaces*, que fornecem cada um nome completo que pode ser referenciado.

Por exemplo, as [`H`](xref:microsoft.quantum.intrinsic.h) [`MResetZ`](xref:microsoft.quantum.measurement.mresetz) operações e são encontradas nos [`Microsoft.Quantum.Instrinsic`](xref:microsoft.quantum.intrinsic) [`Microsoft.Quantum.Measurement`](xref:microsoft.quantum.measurement) namespaces e (parte das [bibliotecas padrão de Q #](xref:microsoft.quantum.qsharplibintro)).
Assim, eles sempre podem ser chamados por meio de *full* seus nomes completos `Microsoft.Quantum.Intrinsic.H(<qubit>)` e `Microsoft.Quantum.Measurement.MResetZ(<qubit>)` , mas sempre fazer isso levaria a um código muito confuso.

Em vez disso, `open` as instruções permitem que os chamadores sejam referenciados com uma abreviação mais concisa, como fizemos no corpo da operação acima.
Portanto, o arquivo inteiro Q # que contém nossa operação consistiria em definir nosso próprio namespace, abrir os namespaces para aqueles que podem ser chamados pela operação e, em seguida, nossa operação:

```qsharp
namespace NamespaceName {
    open Microsoft.Quantum.Intrinsic;     // for the H operation
    open Microsoft.Quantum.Measurement;   // for MResetZ

    operation MeasureSuperposition() : Result {
        using (q = Qubit()) { 
            H(q);
            return MResetZ(q);
        }
    }
}
```

> [!NOTE]
> Os namespaces também podem ser *alias* quando abertos, o que pode ser útil se os nomes de tipo/callable em dois namespaces entrarem em conflito.
> Por exemplo, poderíamos usar `open Microsoft.Quantum.Instrinsic as NamespaceWithH;` acima e, em seguida, chamar `H` via `NamespaceWithH.H(<qubit>)` .

> [!NOTE]
> Uma exceção a tudo disso é o [`Microsoft.Quantum.Core`](xref:microsoft.quantum.core) namespace, que é sempre aberto automaticamente.
> Portanto, os chamadores como o [`Length`](xref:microsoft.quantum.core.length) sempre podem ser usados diretamente.

### <a name="execution-on-target-machines"></a>Execução em computadores de destino

Agora o modelo de execução geral de um programa Q # fica claro.

<br/>
<img src="../media/hostprograms_general_execution_model.png" alt="Q# program execution diagram" width="400">

Em primeiro lugar, o resgatável específico a ser executado tem acesso a quaisquer outros chamados e tipos definidos no mesmo namespace.
Ele também os acessa de qualquer uma das [bibliotecas de Q #](xref:microsoft.quantum.libraries), mas elas devem ser referenciadas por meio de seu nome completo ou pelo uso de `open` instruções descritas acima.

O próprio callable é executado em um *[computador de destino](xref:microsoft.quantum.machines)*.
Esses computadores de destino podem ser hardwares de Quantum reais ou vários simuladores disponíveis como parte do QDK.
Para nossos objetivos aqui, a máquina de destino mais útil é uma instância do [simulador de estado completo](xref:microsoft.quantum.machines.full-state-simulator), `QuantumSimulator` , que calcula o comportamento do programa como se ele estivesse sendo executado em um computador Quantum sem ruído.

Até agora, descrevemos o que acontece quando um chamado Q # específico é executado.
Independentemente de Q # ser usado em um aplicativo autônomo ou com um programa de host, esse processo geral é mais ou menos o mesmo---, portanto, a flexibilidade do QDK.
As diferenças entre as diferentes maneiras de chamar o kit de desenvolvimento Quantum, portanto, revelam-se em *como* esse Q # callable é chamado para ser executado e de que maneira todos os resultados são retornados.
Mais especificamente, as diferenças giram em volta 
1. indicando qual Q # callableName deve ser executada,
2. como possíveis argumentos chamáveis são fornecidos,
3. especificando o computador de destino no qual será executado, e
4. como os resultados são retornados.

Primeiro, discutiremos como isso é feito com o aplicativo autônomo Q # da linha de comando e, em seguida, continue usando programas de host Python e C#.
Reservamos o aplicativo autônomo de Jupyter notebooks do Q # para o último, porque ao contrário dos três primeiros, a funcionalidade principal não é centralizada em um arquivo Q # local.

> [!NOTE]
> Embora não o ilustre nesses exemplos, uma semelhança entre os métodos de execução é que todas as mensagens impressas de dentro do programa Q # (por [`Message`](xref:microsoft.quantum.intrinsic.message) [`DumpMachine`](xref:microsoft.quantum.diagnostics.dumpmachine) exemplo, ou) normalmente serão sempre impressas no respectivo console.

## <a name="q-from-the-command-line"></a>Q # da linha de comando
Uma das maneiras mais fáceis de começar a escrever programas de Q # é evitar a preocupação com arquivos separados e uma segunda linguagem completamente.
O uso do Visual Studio Code ou do Visual Studio com a extensão QDK permite um fluxo de trabalho contínuo no qual executamos Q # que pode ser chamado apenas de um único arquivo Q #.

Para isso, finalmente invocaremos a execução do programa digitando
```dotnetcli
dotnet run
```
na linha de comando.
O fluxo de trabalho mais simples é quando o local do diretório do terminal é o mesmo que o arquivo Q #, que pode ser facilmente manipulado junto com a edição de arquivo Q # usando o terminal integrado no VS Code, por exemplo.
No entanto, o [ `dotnet run` comando](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) aceita inúmeras opções e o programa também pode ser executado de um local diferente, simplesmente fornecendo `--project <PATH>` o local do arquivo Q #.


### <a name="add-entry-point-to-q-file"></a>Adicionar ponto de entrada ao arquivo Q #

A maioria dos arquivos de Q # conterá mais de um callable, por isso naturalmente, precisamos permitir que o compilador saiba *qual* callable pode ser executado quando fornecer o `dotnet run` comando.
Isso é feito com uma simples alteração no próprio arquivo Q #: 
    - Adicione uma linha com `@EntryPoint()` diretamente antes do callable.

Portanto, nosso arquivo acima se tornaria
```qsharp
namespace NamespaceName {
    open Microsoft.Quantum.Intrinsic;     // for the H operation
    open Microsoft.Quantum.Measurement;   // for MResetZ

    @EntryPoint()
    operation MeasureSuperposition() : Result {
        using (q = Qubit()) { 
            H(q);
            return MResetZ(q);
        }
    }
}
```

Agora, uma chamada de `dotnet run` da linha de comando leva a ser `MeasureSuperposition` executada e o valor retornado é impresso diretamente no terminal.
Portanto, você verá ou será `One` `Zero` impresso. 

Observe que não importa se você tiver mais chamadores definidos abaixo dele, somente `MeasureSuperposition` será executado.
Além disso, não é problema se seu callable incluir [comentários de documentação](xref:microsoft.quantum.guide.filestructure#documentation-comments) antes de sua declaração, o `@EntryPoint()` atributo pode ser simplesmente colocado acima deles.

### <a name="callable-arguments"></a>Argumentos que podem ser chamados

Até agora, consideramos apenas uma operação que não usa entradas.
Suponha que queríamos executar uma operação semelhante, mas em várias qubits---o número de que é fornecido como um argumento.
Tal operação poderia ser gravada como
```qsharp
    operation MeasureSuperpositionArray(n : Int) : Result[] {
        using (qubits = Qubit[n]) {              // allocate a register of n qubits
            ApplyToEach(H, qubits);              // apply H to each qubit in the register
            return ForEach(MResetZ, qubits);     // perform MResetZ on each qubit, returns the resulting array
        }
    }
```
onde o valor retornado é uma matriz dos resultados da medição.
Observe que [`ApplyToEach`](xref:microsoft.quantum.canon.applytoeach) e [`ForEach`](xref:microsoft.quantum.arrays.foreach) estão nos [`Microsoft.Quantum.Canon`](xref:microsoft.quantum.canon) [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) namespaces e, exigindo instruções adicionais `open` para cada um.

Se movermos o `@EntryPoint()` atributo para preceder essa nova operação (Observe que só pode haver uma linha em um arquivo), tentar executá-la com simplesmente `dotnet run` resulta em uma mensagem de erro que indica quais opções de linha de comando adicionais são necessárias e como expressá-las.

O formato geral para a linha de comando é realmente `dotnet run [options]` , e os argumentos que podem ser chamados são fornecidos lá.
Nesse caso, o argumento `n` está ausente e mostra que precisamos fornecer a opção `-n <n>` . Para executar o `MeasureSuperpositionArray` para `n=4` qubits, portanto, usamos

```dotnetcli
dotnet run -n 4
```

produzindo uma saída semelhante a

```output
[Zero,One,One,One]
```

É claro que isso se estende a vários argumentos.

> [!NOTE]
> Os nomes de argumentos definidos em `camelCase` são ligeiramente alterados pelo compilador para serem aceitos como entradas de Q #. Por exemplo, se em vez de `n` , usamos o nome `numQubits` acima, essa entrada seria fornecida na linha de comando via `--num-qubits 4` em vez de `-n 4` .

A mensagem de erro também fornece outras opções que podem ser usadas, incluindo como alterar o computador de destino.

### <a name="different-target-machines"></a>Computadores de destino diferentes

Como as saídas de nossas operações até agora têm sido os resultados esperados de sua ação em qubits reais, fica claro que o computador de destino padrão da linha de comando é o simulador de quauntum de estado completo, `QuantumSimulator` .
No entanto, podemos instruir os chamadores a serem executados em um computador de destino específico com a opção `--simulator` (ou a abreviação `-s` ).

Por exemplo, poderíamos executá-lo em [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) :

```dotnetcli
dotnet run -n 4 -s ResourcesEstimator
```

A saída impressa é, então,

```output
Metric          Sum
CNOT            0
QubitClifford   4
R               0
Measure         4
T               0
Depth           0
Width           4
BorrowedWidth   0
```

Para obter detalhes sobre o que essas métricas indicam, consulte [avaliador de recursos: métricas relatadas](xref:microsoft.quantum.machines.resources-estimator#metrics-reported).

### <a name="command-line-execution-summary"></a>Resumo da execução de linha de comando
<br/>
<img src="../media/hostprograms_command_line_diagram.png" alt="Q# program from command line" width="700">

### <a name="non-q-dotnet-run-options"></a>Opções de não-Q # `dotnet run`

Como mencionamos brevemente acima com a `--project` opção, o [ `dotnet run` comando](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) também aceita opções não relacionadas aos argumentos que podem ser chamados por Q #.
Se fornecer ambos os tipos de opções, as `dotnet` opções específicas devem ser fornecidas primeiro, seguidas por um delimitador `--` e, em seguida, as opções específicas de Q #.
Por exemplo, especificar um caminho junto com um número qubits para a operação acima seria executado via `dotnet run --project <PATH> -- -n <n>` .

## <a name="q-with-host-programs"></a>Q # com programas de host

Com nosso arquivo Q # em mãos, uma alternativa para chamar uma operação ou função diretamente da linha de comando é usar um *programa de host* em outra linguagem clássica. Especificamente, isso pode ser feito com Python ou uma linguagem .NET, como C# ou F # (para fins de brevidade, só detalharemos C# aqui).
Um pouco mais de configuração é necessário para habilitar a interoperabilidade, mas esses detalhes podem ser encontrados nos [guias de instalação](xref:microsoft.quantum.install).

Resumindo, a situação agora inclui um arquivo de programa host (por exemplo, `*.py` ou `*.cs` ) no mesmo local que o nosso arquivo Q #.
Agora é o programa *host* que é executado e, no decorrer da sua execução, ele pode chamar operações q # específicas e funções do arquivo q #.
O núcleo da interoperabilidade baseia-se no compilador Q #, tornando o conteúdo do arquivo Q # acessível ao programa de host para que ele possa ser chamado.

Um dos principais benefícios do uso de um programa de host é que os dados clássicos retornados pelo programa Q # podem ser processados ainda mais no idioma do host.
Isso pode consistir em um processamento de dados avançado (por exemplo, algo que não pode ser executado internamente em Q #) e, em seguida, chamar outras ações de Q # com base nesses resultados, ou algo tão simples quanto plotar os resultados de Q #.

O esquema geral é mostrado aqui e discutimos as implementações específicas para Python e C# abaixo. Um exemplo que usa um programa de host F # pode ser encontrado em [exemplos de interoperabilidade .net](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet).

<br/>
<img src="../media/hostprograms_host_program_diagram.png" alt="Q# program from a host program" width="700">

> [!NOTE]
> O `@EntryPoint()` atributo usado para os aplicativos de linha de comando Q # não pode ser usado com programas de host.
> Um erro será gerado se estiver presente no arquivo Q # que está sendo chamado por um host. 

Para trabalhar com diferentes programas de host, não há nenhuma alteração necessária para um `*.qs` arquivo Q #.
As implementações do programa host a seguir funcionam com o mesmo arquivo Q #:

```qsharp
namespace NamespaceName {
    open Microsoft.Quantum.Intrinsic;     // contains H
    open Microsoft.Quantum.Measurement;   // MResetZ
    open Microsoft.Quantum.Canon;         // ApplyToEach
    open Microsoft.Quantum.Arrays;        // ForEach

    operation MeasureSuperposition() : Result {
        using (q = Qubit()) { 
            H(q);
            return MResetZ(q);
        }
    }

    operation MeasureSuperpositionArray(n : Int) : Result[] {
        using (qubits = Qubit[n]) {  
            ApplyToEach(H, qubits); 
            return ForEach(MResetZ, qubits);    
        }
    }
}
```

Selecione a guia correspondente ao seu idioma de host de interesse.

### <a name="python"></a>[Python](#tab/tabid-python)
Um programa de host do Python é construído da seguinte maneira:
1. Importe o `qsharp` módulo, que registra o carregador de módulo para interoperabilidade do Q #. 
    Isso permite que os namespaces Q # apareçam como módulos Python, dos quais é possível "importar" Q # callablefiles.
    Observe que não é tecnicamente os chamadores Q # que são importados, mas em vez de stubs do Python que permitem chamá-los.
    Eles se comportam como objetos de classes python, nos quais usamos métodos para especificar os computadores de destino para os quais enviar a operação para execução.

2. Importe os chamadores Q # que invocaremos diretamente---nesse caso `MeasureSuperposition` e `MeasureSuperpositionArray` .
    ```python
    import qsharp
    from NamespaceName import MeasureSuperposition, MeasureSuperpositionArray
    ```
    Com o `qsharp` módulo importado, você também pode importar os chamadores diretamente dos namespaces da biblioteca do Q #.

3. Entre qualquer outro código Python, agora você pode chamar aqueles que podem ser chamados em computadores de destino específicos e atribuir seus retornos a variáveis (se eles retornarem um valor) para uso posterior.

#### <a name="specifying-target-machines"></a>Especificando computadores de destino
Chamar uma operação a ser executada em um computador de destino específico é feito por meio de métodos de Python diferentes no objeto importado.
Por exemplo, `.simulate(<args>)` , usa o `QuantumSimulator` para executar a operação, enquanto `.estimate_resources(<args>)` faz isso no `ResourcesEstimator` .

#### <a name="passing-inputs-to-q"></a>Passando entradas para Q\#
Os argumentos para o ponto de chamada Q # devem ser fornecidos na forma de um argumento de palavra-chave, em que a palavra-chave é o nome do argumento na definição do tipo "p # chamável".
Ou seja, `MeasureSuperpositionArray.simulate(n=4)` é válido, enquanto `MeasureSuperpositionArray.simulate(4)` geraria um erro.

Portanto, o programa de host do Python 

```python
import qsharp
from NamespaceName import MeasureSuperposition, MeasureSuperpositionArray

single_qubit_result = MeasureSuperposition.simulate()
single_qubit_resources = MeasureSuperposition.estimate_resources()

multi_qubit_result = MeasureSuperpositionArray.simulate(n=4)
multi_qubit_resources = MeasureSuperpositionArray.estimate_resources(n=4)

print('Single qubit:\n' + str(single_qubit_result))
print(single_qubit_resources)

print('\nMultiple qubits:\n' + str(multi_qubit_result))
print(multi_qubit_resources)
```

resulta em uma saída semelhante à seguinte:

```python
Single qubit:
1
{'CNOT': 0, 'QubitClifford': 1, 'R': 0, 'Measure': 1, 'T': 0, 'Depth': 0, 'Width': 1, 'BorrowedWidth': 0}

Multiple qubits:
[0, 1, 1, 1]
{'CNOT': 0, 'QubitClifford': 4, 'R': 0, 'Measure': 4, 'T': 0, 'Depth': 0, 'Width': 4, 'BorrowedWidth': 0}
```

### <a name="c"></a>[C#](#tab/tabid-csharp)

Um programa de host C# tem vários componentes e funciona muito bem com alguns componentes do QDK, como os simuladores, que são criados em C#.

O compilador Q # funciona aqui gerando um namespace C# nomeado de maneira equivalente do namespace Q # em nosso arquivo Q #.
Ele gera ainda mais uma classe C# nomeada de maneira equivalente para cada um dos tipos ou chamadores Q # definidos aqui.

Primeiro, fazemos todas as classes usadas em nosso programa host disponível com `using` instruções, que são aproximadamente análogo às `open` instruções em nosso arquivo Q #:

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;    // contains the target machines (e.g. QuantumSimulator, ResourcesEstimator)
using NamespaceName;                              // make the Q# namespace available
```

Em seguida, declaramos nosso namespace C#, alguns outros bits e partes (Confira o bloco de código completo abaixo) e, em seguida, qualquer programação clássica que desejamos (por exemplo, computação de argumentos para os chamadores Q #).
O último não é necessário em nosso caso, mas um exemplo desse uso pode ser encontrado no [exemplo de interoperabilidade do .net](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet).

#### <a name="target-machines"></a>Computadores de destino

Voltando para a Q #, devemos criar uma instância de qualquer máquina de destino em que executaremos nossas operações.

```csharp
            using var sim = new QuantumSimulator();
```

O uso de outros computadores de destino é tão simples quanto criar uma instância de um diferente, embora a maneira de fazer isso e processar os retornos possa ser um pouco diferente.
Para fins de brevidade, vamos para o [`QuantumSimulator`](xref:microsoft.quantum.machines.full-state-simulator) por enquanto, e incluímos o [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) [seguinte](#including-the-resources-estimator).

Cada classe C# gerada a partir das operações Q # tem um `Run` método, o primeiro argumento do qual deve ser a instância do computador de destino.
Portanto, para executar `MeasureSuperposition` no `QuantumSimulator` , usamos `MeasureSuperposition.Run(sim)` .
Os resultados retornados podem então ser atribuídos a variáveis em C#:

```csharp
            var singleQubitResult = await MeasureSuperposition.Run(sim);
```

> [!NOTE]
> O `Run` método é executado de forma assíncrona porque esse será o caso de hardware Quantum real e, portanto, a `await` palavra-chave bloqueará a execução adicional até que a tarefa seja concluída.

Se o chamado p # não tiver nenhum retorno (ou seja, tiver tipo de retorno `Unit` ), a execução ainda poderá ser feita da mesma maneira sem atribuí-lo a uma variável.
Nesse caso, a linha inteira consistiria simplesmente de 
```csharp
await <callable>.Run(<simulator>);
```

#### <a name="arguments"></a>Argumentos

Qualquer argumento para o Q # callable é simplesmente passado como argumentos adicionais após o computador de destino.
Portanto, os resultados de `MeasureSuperpositionArray` em `n=4` qubits seriam buscados por meio de 

```csharp
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);
```

Um programa completo de host C# poderia, portanto, parecer

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;
using NamespaceName;

namespace host
{
    static class Program
    {
        static async Task Main(string[] args)
        {
            using var sim = new QuantumSimulator();

            var singleQubitResult = await MeasureSuperposition.Run(sim);
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);

            Console.WriteLine($"Single qubit result: {singleQubitResult}");
            Console.WriteLine($"Multiple qubit result: {multiQubitResult}");
        }
    }
}
```

No local do arquivo C#, o programa de host pode ser executado na linha de comando digitando
```dotnetcli
dotnet run
```
e, nesse caso, você verá a saída gravada no console semelhante a 
```output
Single qubit result: One
Multiple qubit result: [One,One,Zero,Zero]
```

> [!NOTE]
> Devido à interoperabilidade do compilador com namespaces, poderíamos também tornar os chamadores do Q # disponíveis sem a `using NamespaceName;` instrução e simplesmente corresponder o título do namespace do C# a ele.
> Ou seja, substituindo `namespace host` por `namespace NamespaceName` .

#### <a name="including-the-resources-estimator"></a>Incluindo o estimador de recursos

O [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) requer uma implementação um pouco diferente para recuperar a saída.

Em primeiro lugar, em vez de instanciá-los como uma variável com uma `using` instrução (como fazemos com o `QuantumSimulator` ), nós criamos mais diretamente objetos da classe por meio de

```csharp
            var estimatorSingleQ = new ResourcesEstimator();
            var estimatorMultiQ = new ResourcesEstimator();
```

Observe que, em vez de um único simulador de destino a ser usado por várias operações Q #, criamos uma instância de cada uma delas. Isso ocorre porque os próprios objetos são modificados quando usados como computadores de destino, e seus resultados podem ser recuperados posteriormente com o método de classe `.ToTSV()` .

Para executar as operações nos estimadores de recursos, usamos

```csharp
            await MeasureSuperposition.Run(estimatorSingleQ);
            await MeasureSuperpositionArray.Run(estimatorMultiQ, 4);
```
e, em seguida, busque os resultados como valores separados por tabulação (TSV) com `estimatorSingleQ.ToTSV()` e `estimatorMultiQ.ToTSV()` .

Portanto, um programa de host C# completo que usa ambos `QuantumSimulator` e `ResourcesEstimator` poderia ter a forma:

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;
using NamespaceName;

namespace host
{
    static class Program
    {
        static async Task Main(string[] args)
        {
            using var sim = new QuantumSimulator();
            var estimatorSingleQ = new ResourcesEstimator();
            var estimatorMultiQ = new ResourcesEstimator();

            var singleQubitResult = await MeasureSuperposition.Run(sim);
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);

            await MeasureSuperposition.Run(estimatorSingleQ);
            await MeasureSuperpositionArray.Run(estimatorMultiQ, 4);

            Console.WriteLine($"Single qubit result: {singleQubitResult}");
            Console.WriteLine("Single qubit resources:");
            Console.WriteLine(estimatorSingleQ.ToTSV());

            Console.WriteLine($"\nMultiple qubit result: {multiQubitResult}");
            Console.WriteLine("Multiple qubit resources:");
            Console.WriteLine(estimatorMultiQ.ToTSV());
        }
    }
}
```


que produziria uma saída semelhante a

```output
Single qubit result: One
Single qubit resources:
Metric          Sum
CNOT            0
QubitClifford   1
R               0
Measure         1
T               0
Depth           0
Width           1
BorrowedWidth   0

Multiple qubit result: [One,One,One,Zero]
Multiple qubit resources:
Metric          Sum
CNOT            0
QubitClifford   4
R               0
Measure         4
T               0
Depth           0
Width           4
BorrowedWidth   0
```

***

## <a name="q-jupyter-notebooks"></a>Jupyter Notebooks do Q#
Os blocos de anotações do Q # Jupyter usam o kernel IQ #, que permite que você defina, compile e execute os chamadores Q # em um único bloco de anotações---tudo junto com as instruções, as anotações e outros tipos de conteúdo.
Isso significa que, embora seja possível importar e usar o conteúdo de `*.qs` arquivos Q #, eles não são necessários no modelo de execução.

Aqui, detalharemos como executar as operações de Q # definidas acima, mas uma introdução mais ampla ao uso de notebooks com Q # Jupyter é fornecida em [introdução aos notebooks q # e Jupyter](https://github.com/microsoft/Quantum/blob/master/samples/getting-started/intro-to-iqsharp/Notebook.ipynb).

### <a name="defining-operations"></a>Definindo operações

Em um Jupyter Notebook de Q #, você insere o código de Q # da mesma forma que faria dentro do namespace de um arquivo Q #.

Portanto, podemos habilitar o acesso a callables das [bibliotecas padrão do Q #](xref:microsoft.quantum.qsharplibintro) com `open` instruções para seus respectivos namespaces.
Após a execução de uma célula com tal instrução, as definições desses namespaces estão disponíveis em todo o espaço de trabalho.

> [!NOTE]
> Os chamados de [Microsoft. Quantum. intrínseco](xref:microsoft.quantum.intrinsic) e [Microsoft. Quantum. Canon](xref:microsoft.quantum.canon) (por exemplo, [`H`](xref:microsoft.quantum.intrinsic.h) e [`ApplyToEach`](xref:microsoft.quantum.canon.applytoeach) ) estão automaticamente disponíveis para operações definidas em células nos blocos de anotações do Q # Jupyter.
> No entanto, isso não é verdadeiro para o código trazido de arquivos de origem Q # externos (um processo mostrado em [introdução aos notebooks Jupyter e q #](https://github.com/microsoft/Quantum/blob/master/samples/getting-started/intro-to-iqsharp/Notebook.ipynb)). 
> 

Da mesma forma, a definição de operações requer apenas a gravação do código Q # e a execução da célula.

<img src="../media/hostprograms_jupyter_op_def_crop.png" alt="Jupyter cell defining Q# operations" width="600">

Em seguida, a saída lista essas operações, que podem ser chamadas a partir de células futuras.

### <a name="target-machines"></a>Computadores de destino

A funcionalidade para executar operações em computadores de destino específicos é fornecida por meio de [comandos do IQ # Magic](xref:microsoft.quantum.guide.quickref.iqsharp).
Por exemplo, utiliza `%simulate` o `QuantumSimulator` e `%estimate` usa o `ResourcesEstimator` :

<img src="../media/hostprograms_jupyter_no_args_sim_est_crop.png" alt="Simulate and estimate resources Jupyter cell" width="500">

### <a name="passing-inputs-to-functions-and-operations"></a>Passando entradas para funções e operações

Atualmente, os comandos mágicos de execução só podem ser usados com operações que não usam argumentos. Portanto, para executar `MeasureSuperpositionArray` , precisamos definir uma operação "wrapper" que chama a operação com os argumentos:

<img src="../media/hostprograms_jupyter_wrapper_def_sim_crop.png" alt="Wrapper function and simulate Jupyter cell" width="550">

É claro que essa operação pode ser usada de forma semelhante com `%estimate` e outros comandos de execução.
