---
title: Testando e depurando
description: Saiba como usar testes de unidade, fatos e asserções e funções de despejo para testar e depurar programas Quantum.
author: tcNickolas
ms.author: mamykhai@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.guide.testingdebugging
ms.openlocfilehash: dd6c7ae8a016423f26c37f3eedf0ae9c1d126b78
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630022"
---
# <a name="testing-and-debugging"></a>Testando e depurando

Assim como acontece com a programação clássica, é essencial poder verificar se os programas Quantum atuam como pretendidos e ser capaz de diagnosticar um programa Quantum incorreto.
Nesta seção, abordaremos as ferramentas oferecidas por Q # para testar e depurar programas Quantum.

## <a name="unit-tests"></a>Testes de Unidade

Uma abordagem comum para testar programas clássicos é escrever programas pequenos chamados *testes de unidade* que executam código em uma biblioteca e comparam sua saída a alguma saída esperada.
Por exemplo, talvez queiramos garantir que `Square(2)` retorne `4` , já que sabemos *um priori* que é de $2 ^ 2 = $4.

O Q # dá suporte à criação de testes de unidade para programas Quantum e que pode ser executado como testes dentro da estrutura de teste de unidade do [xUnit](https://xunit.github.io/) .

### <a name="creating-a-test-project"></a>Criando um projeto de teste

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Abra o Visual Studio 2019. Vá para o `File` menu e selecione `New`  >  `Project...` .
No canto superior direito, procure `Q#` e selecione o `Q# Test Project` modelo.

#### <a name="command-line--visual-studio-code"></a>[Linha de comando/Visual Studio Code](#tab/tabid-vscode)

Na sua linha de comando favorita, execute o seguinte comando:
```bash
$ dotnet new xunit -lang Q# -o Tests
$ cd Tests
$ code . # To open in Visual Studio Code
```

****

Seu novo projeto terá um único arquivo `Tests.qs` , que fornece um local conveniente para definir novos testes de unidade do Q #.
Inicialmente, esse arquivo contém um teste de unidade de exemplo `AllocateQubit` que verifica se um qubit alocado recentemente está no {0} estado $ \ket $ e imprime uma mensagem:

```qsharp
    @Test("QuantumSimulator")
    operation AllocateQubit () : Unit {

        using (qubit = Qubit()) {
            Assert([PauliZ], [qubit], Zero, "Newly allocated qubit must be in the |0⟩ state.");
        }
        
        Message("Test passed");
    }
```

: novo: qualquer operação ou função Q # que usa um argumento do tipo `Unit` e retorna `Unit` pode ser marcada como um teste de unidade por meio do `@Test("...")` atributo. O argumento para esse atributo, `"QuantumSimulator"` acima, especifica o destino no qual o teste é executado. Um único teste pode ser executado em vários destinos. Por exemplo, adicione um atributo `@Test("ResourcesEstimator")` acima `AllocateQubit` . 
```qsharp
    @Test("QuantumSimulator")
    @Test("ResourcesEstimator")
    operation AllocateQubit () : Unit {
        ...
```
Salve o arquivo e execute todos os testes. Agora deve haver dois testes de unidade, um em que AllocateQubit é executado no QuantumSimulator e um onde ele é executado no ResourceEstimator. 

O compilador Q # reconhece os destinos internos "QuantumSimulator", "ToffoliSimulator" e "ResourcesEstimator" como destinos de execução válidos para testes de unidade. Também é possível especificar qualquer nome totalmente qualificado para definir um destino de execução personalizado. 

### <a name="running-q-unit-tests"></a>Executando os testes de unidade de Q #

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Como configuração única por solução, vá para o `Test` menu e selecione `Test Settings`  >  `Default Processor Architecture`  >  `X64` .

> [!TIP]
> A configuração de arquitetura de processador padrão para o Visual Studio é armazenada no `.suo` arquivo de opções de solução () para cada solução.
> Se você excluir esse arquivo, precisará selecionar `X64` como a arquitetura do processador novamente.

Compile o projeto, vá para o `Test` menu e selecione `Windows`  >  `Test Explorer` . `AllocateQubit`aparecerá na lista de testes no `Not Run Tests` grupo. Selecione `Run All` ou execute este teste individual e ele deve passar!

#### <a name="command-line--visual-studio-code"></a>[Linha de comando/Visual Studio Code](#tab/tabid-vscode)

Para executar testes, navegue até a pasta do projeto (a pasta que contém `Tests.csproj` ) e execute o comando:

```bash
$ dotnet restore
$ dotnet test
```

Você deve ver um resultado semelhante ao seguinte:

```
Build started, please wait...
Build completed.

Test run for C:\Users\chgranad.REDMOND\tmp\Tests\bin\Debug\netcoreapp2.0\Tests.dll(.NETCoreApp,Version=v2.0)
Microsoft (R) Test Execution Command Line Tool Version 15.3.0-preview-20170628-02
Copyright (c) Microsoft Corporation.  All rights reserved.

Starting test execution, please wait...
[xUnit.net 00:00:00.5864002]   Discovering: Tests
[xUnit.net 00:00:00.7073844]   Discovered:  Tests
[xUnit.net 00:00:00.7453826]   Starting:    Tests
[xUnit.net 00:00:00.9590439]   Finished:    Tests

Total tests: 1. Passed: 1. Failed: 0. Skipped: 0.
Test Run Successful.
Test execution time: 1.9607 Seconds
```

Os testes de unidade podem ser filtrados de acordo com seu nome e/ou o destino de execução:

```bash 
$ dotnet test --filter "Target=QuantumSimulator"
$ dotnet test --filter "Name=AllocateQubit"
```


***

A função intrínseca <xref:microsoft.quantum.intrinsic.message> tem o tipo `(String -> Unit)` e habilita a criação de mensagens de diagnóstico.

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Depois de executar um teste no Test Explorer e clicar no teste, um painel será exibido com informações sobre a execução do teste: passou/falha no status, tempo decorrido e um link de "saída". Se você clicar no link "saída", a saída de teste será aberta em uma nova janela.

![saída de teste](~/media/unit-test-output.png)

#### <a name="command-line--visual-studio-code"></a>[Linha de comando/Visual Studio Code](#tab/tabid-vscode)

O status de aprovação/reprovação de cada teste é impresso no console do `dotnet test` .
Para testes com falha, as saídas também são impressas no console do para ajudar a diagnosticar a falha.

***

## <a name="facts-and-assertions"></a>Fatos e asserções

Como as funções em Q # não têm efeitos colaterais _lógicos_ , quaisquer _outros tipos_ de efeitos de execução de uma função cujo tipo de saída é a tupla vazia `()` nunca podem ser observados em um programa Q #.
Ou seja, um computador de destino pode optar por não executar nenhuma função que retorna `()` com a garantia de que essa omissão não modificará o comportamento de qualquer código Q # a seguir.
Isso torna as funções retornando `()` (ou seja, `Unit` ) uma ferramenta útil para inserir asserções e depurar a lógica em programas Q #. 

Vamos considerar um exemplo simples:

```qsharp
function PositivityFact(value : Double) : Unit 
{
    if (value <= 0) 
    {
        fail "Expected a positive number.";
    }
}
```

Aqui, a palavra-chave `fail` indica que a computação não deve continuar, gerando uma exceção no computador de destino que executa o programa Q #.
Por definição, uma falha desse tipo não pode ser observada em Q #, pois nenhum código Q # adicional é executado depois que uma `fail` instrução é atingida.
Portanto, se continuarmos passando por uma chamada para `PositivityFact` , podemos ter certeza de que sua entrada era positiva.

Observe que podemos implementar o mesmo comportamento que `PositivityFact` usar a [`Fact`](xref:microsoft.quantum.diagnostics.fact) função do <xref:microsoft.quantum.diagnostics> namespace:

```qsharp
    Fact(value <= 0, "Expected a positive number.");
```

As *asserções*, por outro lado, são usadas de forma semelhante aos fatos, mas podem ser dependentes do estado do computador de destino. De forma correspondente, eles são definidos como operações, enquanto os fatos são definidos como funções (como acima).
Para entender a distinção, considere o seguinte uso de um fato em uma asserção:

```qsharp
operation AssertQubitsAreAvailable() : Unit
{
     Fact(GetQubitsAvailableToUse() > 0, "No qubits were actually available");
}
```

Aqui, estamos usando a operação <xref:microsoft.quantum.environment.getqubitsavailabletouse> para retornar o número de qubits disponíveis para uso.
Como isso depende claramente do estado global do programa e de seu ambiente de execução, nossa definição de `AssertQubitsAreAvailable` deve ser uma operação também.
No entanto, podemos usar esse estado global para gerar um `Bool` valor simples como entrada para a `Fact` função.

Com base nessas ideias, [o prelúdio](xref:microsoft.quantum.libraries.standard.prelude) oferece duas declarações especialmente úteis <xref:microsoft.quantum.intrinsic.assert> e <xref:microsoft.quantum.intrinsic.assertprob> modeladas como operações no `()` . Cada declaração assume um operador Pauli que descreve uma medida de interesse específica, um registro Quantum no qual uma medida deve ser executada e um resultado hipotético.
Em computadores de destino que funcionam por simulação, não estamos vinculados pelo [teorema no-Cloning](https://en.wikipedia.org/wiki/No-cloning_theorem)e podem executar essas medições sem perturbar o registro passado para tais asserções.
Um simulador pode, assim, ser semelhante à `PositivityFact` função acima, anular a computação se o resultado hipotético não fosse observado na prática:

```qsharp
using (register = Qubit()) 
{
    H(register);
    Assert([PauliX], [register], Zero);
    // Even though we do not have access to states in Q#,
    // we know by the anthropic principle that the state
    // of register at this point is |+〉.
}
```

Em hardware Quantum físico, em que o teorema sem clonagem impede o exame do estado Quantum, as `Assert` `AssertProb` operações e simplesmente retornam `()` sem nenhum outro efeito.

O <xref:microsoft.quantum.diagnostics> namespace fornece várias outras funções da `Assert` família que nos permitem verificar condições mais avançadas. 

## <a name="dump-functions"></a>Funções de despejo

Para ajudar a solucionar problemas de programas Quantum, o <xref:microsoft.quantum.diagnostics> namespace oferece duas funções que podem ser despejadas em um arquivo o status atual do computador de destino: <xref:microsoft.quantum.diagnostics.dumpmachine> e <xref:microsoft.quantum.diagnostics.dumpregister> . A saída gerada de cada uma depende do computador de destino.

### <a name="dumpmachine"></a>DumpMachine

O simulador de Quantum completo distribuído como parte do kit de desenvolvimento Quantum grava no arquivo a [função de onda](https://en.wikipedia.org/wiki/Wave_function) de todo o sistema Quantum, como uma matriz unidimensional de números complexos, na qual cada elemento representa a amplitude da probabilidade de medir o estado de base computacional $ \ket{n} $, em que $ \ket{n} = \ket{b_ {n-1}... b_1b_0} $ para bits $ \{ b_i \} $. Por exemplo, em um computador com apenas dois qubits alocados e no estado Quantum $ $ \begin{align} \ket{\psi} = \frac {1} {\sqrt {2} } \ket {00} -\frac{(1 + i)} {2} \ket {10} , \end{align} $ $ Calling <xref:microsoft.quantum.diagnostics.dumpmachine> gera essa saída:

```
# wave function for qubits with ids (least to most significant): 0;1
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣2❭:    -0.500000 + -0.500000 i  ==     **********           [ 0.500000 ]   /     [ -2.35619 rad ]
∣3❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

A primeira linha fornece um comentário com as IDs do qubits correspondente em sua ordem significativa.
O restante das linhas descreve a amplitude de probabilidade de medir o vetor de estado base $ \ket{n} $ nos formatos cartesianas e polar. Em detalhes para a primeira linha:

* **`∣0❭:`** Esta linha corresponde ao `0` estado de base computacional
* **`0.707107 +  0.000000 i`**: a amplitude de probabilidade no formato cartesiano.
* **` == `**: o `equal` sinal separa as representações equivalentes.
* **`**********  `**: Uma representação gráfica da magnitude, o número de `*` é proporcional à probabilidade de medir esse vetor de estado.
* **`[ 0.500000 ]`**: o valor numérico da magnitude
* **`    ---`**: Uma representação gráfica da fase da amplitude (veja abaixo).
* **`[ 0.0000 rad ]`**: o valor numérico da fase (em radianos).

A magnitude e a fase são exibidas com uma representação gráfica. A representação de magnitude é direta: ela mostra uma barra de `*` , quanto maior a probabilidade, maior será o tamanho da barra. Para a fase, mostramos os seguintes símbolos para representar o ângulo com base em intervalos:

```
[ -π/16,   π/16)       ---
[  π/16,  3π/16)        /-
[ 3π/16,  5π/16)        / 
[ 5π/16,  7π/16)       +/ 
[ 7π/16,  9π/16)      ↑   
[ 8π/16, 11π/16)    \-    
[ 7π/16, 13π/16)    \     
[ 7π/16, 15π/16)   +\     
[15π/16, 19π/16)   ---    
[17π/16, 19π/16)   -/     
[19π/16, 21π/16)    /     
[21π/16, 23π/16)    /+    
[23π/16, 25π/16)      ↓   
[25π/16, 27π/16)       -\ 
[27π/16, 29π/16)        \ 
[29π/16, 31π/16)        \+
[31π/16,   π/16)       ---
```

Os exemplos a seguir mostram `DumpMachine` alguns Estados comuns:

### `∣0❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

### `∣1❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣1❭:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
```

### `∣+❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]      --- [  0.00000 rad ]
∣1❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]      --- [  0.00000 rad ]
```

### `∣-❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]      --- [  0.00000 rad ]
∣1❭:    -0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]  ---     [  3.14159 rad ]
```


  > [!NOTE]
  > A ID de um qubit é atribuída em tempo de execução e não está necessariamente alinhada com a ordem na qual o qubit foi alocado ou sua posição em um registro qubit.


#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

  > [!TIP]
  > Você pode descobrir uma ID de qubit no Visual Studio colocando um ponto de interrupção em seu código e inspecionando o valor de uma variável qubit, por exemplo:
  > 
  > ![Mostrar ID do qubit no Visual Studio](~/media/qubit_id.png)
  >
  > o qubit com índice `0` em `register2` tem ID = `3` , o qubit com índice `1` tem ID = `2` .

#### <a name="command-line--visual-studio-code"></a>[Linha de comando/Visual Studio Code](#tab/tabid-vscode)

  > [!TIP]
  > Você pode descobrir uma ID de qubit usando a <xref:microsoft.quantum.intrinsic.message> função e passando a variável qubit na mensagem, por exemplo:
  >
  > ```qsharp
  > Message($"0={register2[0]}; 1={register2[1]}");
  > ```
  > 
  > que pode gerar essa saída:
  >```
  > 0=q:3; 1=q:2
  >```
  > Isso significa que o qubit com índice `0` em `register2` tem ID = `3` , o qubit com índice `1` tem a ID = `2` .


***

<xref:microsoft.quantum.diagnostics.dumpmachine>faz parte do <xref:microsoft.quantum.diagnostics> namespace, portanto, para usá-lo, você deve adicionar uma `open` instrução:

```qsharp
namespace Samples {
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;

    operation Operation () : Unit {
        using (qubits = Qubit[2]) {
            H(qubits[1]);
            DumpMachine("dump.txt");
        }
    }
}
```


### <a name="dumpregister"></a>DumpRegister

<xref:microsoft.quantum.diagnostics.dumpregister>funciona como <xref:microsoft.quantum.diagnostics.dumpmachine> , exceto que ele também usa uma matriz de qubits para limitar a quantidade de informações apenas às relevantes para o qubits correspondente.

Assim como acontece com <xref:microsoft.quantum.diagnostics.dumpmachine> , as informações geradas <xref:microsoft.quantum.diagnostics.dumpregister> dependem do computador de destino. Para o simulador de Quantum de estado completo, ele grava no arquivo a função de onda até uma fase global do subsistema Quantum gerado pelo qubits fornecido no mesmo formato que <xref:microsoft.quantum.diagnostics.dumpmachine> .  Por exemplo, pegue novamente um computador com apenas dois qubits alocados e no estado Quantum $ $ \begin{align} \ket{\psi} = \frac {1} {\sqrt {2} } \ket {00} -\frac{(1 + i)} {2} \ket {10} =-e ^ {-i \ pi/4} ((\frac {1} {\sqrt {2} } \ket {0} -\frac{(1 + i)} {2} \ket {1} ) \otimes \frac{-(1 + i)} {\sqrt {2} } \ket {0} ), \end{align} $ $ chamando <xref:microsoft.quantum.diagnostics.dumpregister> para `qubit[0]` gera esta saída:

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:    -0.707107 + -0.707107 i  ==     ******************** [ 1.000000 ]  /      [ -2.35619 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

e chamar <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[1]` gera essa saída:

```
# wave function for qubits with ids (least to most significant): 1
∣0❭:     0.707107 +  0.000000 i  ==     ***********          [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:    -0.500000 + -0.500000 i  ==     ***********          [ 0.500000 ]  /      [ -2.35619 rad ]
```

Em geral, o estado de um registro que é confusas com outro registro é um estado misto em vez de um estado puro. Nesse caso, <xref:microsoft.quantum.diagnostics.dumpregister> o gera a seguinte mensagem:

```
Qubits provided (0;) are entangled with some other qubit.
```

O exemplo a seguir mostra como você pode usar o <xref:microsoft.quantum.diagnostics.dumpregister> e <xref:microsoft.quantum.diagnostics.dumpmachine> o no código do Q #:

```qsharp
namespace app
{
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;

    operation Operation () : Unit {

        using (qubits = Qubit[2]) {
            X(qubits[1]);
            H(qubits[1]);
            R1Frac(1, 2, qubits[1]);
            
            DumpMachine("dump.txt");
            DumpRegister("q0.txt", qubits[0..0]);
            DumpRegister("q1.txt", qubits[1..1]);

            ResetAll(qubits);
        }
    }
}
```

## <a name="debugging"></a>Depuração

Além das `Assert` funções e `Dump` operações, o Q # dá suporte a um subconjunto de recursos de depuração padrão do Visual Studio: [definir pontos de interrupção de linha](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), percorrer [código usando F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) e [inspecionar valores de variáveis clássicas](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) é possível durante a execução do código no simulador.

A depuração no Visual Studio Code aproveita os recursos de depuração fornecidos pelo C# para Visual Studio Code extensão da plataforma OmniSharp e requer a instalação da [versão mais recente](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp). 
