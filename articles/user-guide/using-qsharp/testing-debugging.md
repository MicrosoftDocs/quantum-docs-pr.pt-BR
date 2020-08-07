---
title: Testando e depurando
description: Saiba como usar testes de unidade, fatos e asserções e funções de despejo para testar e depurar programas Quantum.
author: tcNickolas
ms.author: mamykhai@microsoft.com
ms.date: 06/01/2020
ms.topic: article
uid: microsoft.quantum.guide.testingdebugging
no-loc:
- Q#
- $$v
ms.openlocfilehash: 2b5276da594ba263177d435c1153f6d96e29c4e8
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87867906"
---
# <a name="testing-and-debugging"></a>Testando e depurando

Assim como acontece com a programação clássica, é essencial poder verificar se os programas Quantum atuam como pretendidos e podem diagnosticar o comportamento incorreto.
Nesta seção, abordaremos as ferramentas oferecidas pelo Q# para testar e depurar programas Quantum.

## <a name="unit-tests"></a>Testes de Unidade

Uma abordagem comum para testar programas clássicos é escrever programas pequenos chamados de *testes de unidade*, que executam o código em uma biblioteca e comparam sua saída a alguma saída esperada.
Por exemplo, você pode garantir que os `Square(2)` retornos `4` desde que você saiba *um priori* que $2 ^ 2 = $4.

Q#dá suporte à criação de testes de unidade para programas Quantum e que podem ser executados como testes dentro da estrutura de teste de unidade do [xUnit](https://xunit.github.io/) .

### <a name="creating-a-test-project"></a>Criando um projeto de teste

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Abra o Visual Studio 2019. Vá para o menu **arquivo** e selecione **novo > projeto...**. No canto superior direito, procure `Q#` e selecione o modelo projeto de ** Q# teste** .

#### <a name="command-line--visual-studio-code"></a>[Linha de comando/Visual Studio Code](#tab/tabid-vscode)

Na sua linha de comando favorita, execute o seguinte comando:
```dotnetcli
$ dotnet new xunit -lang Q# -o Tests
$ cd Tests
$ code . # To open in Visual Studio Code
```

****

Seu novo projeto tem um único arquivo `Tests.qs` , que fornece um local conveniente para definir novos Q# testes de unidade.
Inicialmente, esse arquivo contém um teste de unidade de exemplo `AllocateQubit` que verifica se um qubit alocado recentemente está no estado $ \ket {0} $ e imprime uma mensagem:

```qsharp
    @Test("QuantumSimulator")
    operation AllocateQubit () : Unit {

        using (qubit = Qubit()) {
            AssertMeasurement([PauliZ], [qubit], Zero, "Newly allocated qubit must be in the |0⟩ state.");
        }
        
        Message("Test passed");
    }
```

Qualquer Q# operação ou função que usa um argumento de tipo `Unit` e retornos `Unit` pode ser marcada como um teste de unidade por meio do `@Test("...")` atributo. No exemplo anterior, o argumento para esse atributo, `"QuantumSimulator"` , especifica o destino no qual o teste é executado. Um único teste pode ser executado em vários destinos. Por exemplo, adicione um atributo `@Test("ResourcesEstimator")` antes de `AllocateQubit` . 
```qsharp
    @Test("QuantumSimulator")
    @Test("ResourcesEstimator")
    operation AllocateQubit () : Unit {
        ...
```
Salve o arquivo e execute todos os testes. Agora deve haver dois testes de unidade, um em que `AllocateQubit` é executado no `QuantumSimulator` e um onde ele é executado no `ResourcesEstimator` . 

O Q# compilador reconhece os destinos internos `"QuantumSimulator"` , `"ToffoliSimulator"` e `"ResourcesEstimator"` como destinos de execução válidos para testes de unidade. Também é possível especificar qualquer nome totalmente qualificado para definir um destino de execução personalizado. 

### <a name="running-no-locq-unit-tests"></a>Executando Q# testes de unidade

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Como configuração única por solução, vá para o menu **teste** e selecione **configurações de teste > arquitetura de processador padrão > x64**.

> [!TIP]
> A configuração de arquitetura de processador padrão para o Visual Studio é armazenada no `.suo` arquivo de opções de solução () para cada solução.
> Se você excluir esse arquivo, precisará selecionar **x64** como a arquitetura do processador novamente.

Crie o projeto, abra o menu **testar** e selecione **Windows > Test Explorer**. **AllocateQubit** é exibido na lista de testes no grupo de **testes não executado** . Selecione **executar tudo** ou executar este teste individual.

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

Os testes de unidade podem ser filtrados de acordo com seu nome ou o destino de execução:

```bash 
$ dotnet test --filter "Target=QuantumSimulator"
$ dotnet test --filter "Name=AllocateQubit"
```


***

A função intrínseca <xref:microsoft.quantum.intrinsic.message> tem o tipo `(String -> Unit)` e habilita a criação de mensagens de diagnóstico.

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Depois de executar um teste no Test Explorer e clicar no teste, um painel será exibido com informações sobre a execução do teste: status de aprovação/falha, tempo decorrido e um link para a saída. Clique em **saída** para abrir a saída de teste em uma nova janela.

![saída de teste](~/media/unit-test-output.png)

#### <a name="command-line--visual-studio-code"></a>[Linha de comando/Visual Studio Code](#tab/tabid-vscode)

O status de aprovação/reprovação de cada teste é impresso no console do `dotnet test` .
Para testes com falha, as saídas também são impressas no console do para ajudar a diagnosticar a falha.

***

## <a name="facts-and-assertions"></a>Fatos e asserções

Como as funções no Q# não têm efeitos colaterais _lógicos_ , você nunca pode observar, de dentro de um Q# programa, quaisquer outros tipos de efeitos da execução de uma função cujo tipo de saída seja a tupla vazia `()` .
Ou seja, um computador de destino pode optar por não executar nenhuma função que retorna `()` com a garantia de que essa omissão não modificará o comportamento de qualquer código a seguir Q# .
Esse comportamento faz com que as funções retornem `()` (como `Unit` ) uma ferramenta útil para incorporar asserções e depurar a lógica em Q# programas. 

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

Aqui, a palavra-chave `fail` indica que a computação não deve continuar e gera uma exceção no computador de destino que executa o Q# programa.
Por definição, uma falha desse tipo não pode ser observada de dentro do Q# , pois o computador de destino não executa mais o Q# código depois de atingir uma `fail` instrução.
Portanto, se continuarmos após uma chamada para `PositivityFact` , poderemos ter certeza de que sua entrada foi positiva.

Observe que podemos implementar o mesmo comportamento que `PositivityFact` usar a [`Fact`](xref:microsoft.quantum.diagnostics.fact) função do <xref:microsoft.quantum.diagnostics> namespace:

```qsharp
    Fact(value > 0, "Expected a positive number.");
```

As *asserções*, por outro lado, são usadas de forma semelhante aos fatos, mas podem depender do estado do computador de destino. De forma correspondente, eles são definidos como operações, enquanto os fatos são definidos como funções (como no exemplo anterior).
Para entender a distinção, considere o seguinte uso de um fato em uma asserção:

```qsharp
operation AssertQubitsAreAvailable() : Unit
{
     Fact(GetQubitsAvailableToUse() > 0, "No qubits were actually available");
}
```

Aqui, estamos usando a operação <xref:microsoft.quantum.environment.getqubitsavailabletouse> para retornar o número de qubits disponíveis para uso.
Como isso depende do estado global do programa e de seu ambiente de execução, nossa definição de `AssertQubitsAreAvailable` deve ser uma operação também.
No entanto, podemos usar esse estado global para gerar um `Bool` valor simples como entrada para a `Fact` função.

[A prelúdio, a](xref:microsoft.quantum.libraries.standard.prelude)criação dessas ideias, oferece duas declarações especialmente úteis <xref:microsoft.quantum.diagnostics.assertmeasurement> e <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> modeladas como operações no `()` . Essas asserções adotam um operador Pauli que descreve uma medição específica de interesse, um registro Quantum no qual uma medida é executada e um resultado hipotético.
Os computadores de destino que trabalham por simulação não são vinculados pelo [teorema no-Cloning](https://en.wikipedia.org/wiki/No-cloning_theorem)e podem executar essas medições sem perturbar o registro que passa para tais asserções.
Um simulador pode, assim, semelhante à `PositivityFact` função anterior, interromper a computação se o resultado hipotético não for observado na prática:

```qsharp
using (register = Qubit()) 
{
    H(register);
    AssertMeasurement([PauliX], [register], Zero);
    // Even though we do not have access to states in Q#,
    // we know by the anthropic principle that the state
    // of register at this point is |+〉.
}
```

Em hardware Quantum físico, em que o teorema no-Cloning impede o exame de um estado Quantum, as `AssertMeasurement` `AssertMeasurementProbability` operações e simplesmente retornam `()` sem nenhum outro efeito.

O <xref:microsoft.quantum.diagnostics> namespace fornece várias outras funções da `Assert` família, com as quais você pode verificar condições mais avançadas. 

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
* **`    ---`**: Uma representação gráfica da fase da amplitude (consulte a saída a seguir).
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
  > A ID de um qubit é atribuída em tempo de execução e não é necessariamente alinhada com a ordem na qual o qubit foi alocado ou sua posição em um registro qubit.


#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

  > [!TIP]
  > Você pode localizar uma ID de qubit no Visual Studio colocando um ponto de interrupção em seu código e inspecionando o valor de uma variável qubit, por exemplo:
  > 
  > ![Mostrar ID do qubit no Visual Studio](~/media/qubit_id.png)
  >
  > o qubit com índice `0` em `register2` tem ID = `3` , o qubit com índice `1` tem ID = `2` .

#### <a name="command-line--visual-studio-code"></a>[Linha de comando/Visual Studio Code](#tab/tabid-vscode)

  > [!TIP]
  > Você pode localizar uma ID de qubit usando a <xref:microsoft.quantum.intrinsic.message> função e passando a variável qubit na mensagem, por exemplo:
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

Como <xref:microsoft.quantum.diagnostics.dumpmachine> o é parte do <xref:microsoft.quantum.diagnostics> namespace, você deve adicionar uma `open` instrução para acessá-lo:

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

<xref:microsoft.quantum.diagnostics.dumpregister>funciona como <xref:microsoft.quantum.diagnostics.dumpmachine> , exceto pelo fato de que ele também usa uma matriz de qubits para limitar a quantidade de informações apenas às relevantes para o qubits correspondente.

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

O exemplo a seguir mostra como você pode usar o <xref:microsoft.quantum.diagnostics.dumpregister> e <xref:microsoft.quantum.diagnostics.dumpmachine> o em seu Q# código:

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

Além das `Assert` funções e `Dump` operações, Q# o oferece suporte a um subconjunto de recursos de depuração padrão do Visual Studio: [definir pontos de interrupção de linha](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), percorrer [código usando F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger)e [inspecionar valores de variáveis clássicas](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) é possível durante a execução do código no simulador.

A depuração no Visual Studio Code aproveita os recursos de depuração fornecidos pelo C# para Visual Studio Code extensão da plataforma OmniSharp e requer a instalação da [versão mais recente](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp). 
