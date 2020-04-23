---
title: Testando e depurando programas Q#
description: Aprenda a usar testes unitários, fatos e afirmações, e funções de despejo para testar e depurar programas quânticos.
author: tcNickolas
ms.author: mamykhai@microsoft.com
uid: microsoft.quantum.techniques.testing-and-debugging
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: caf15b7273b7efed1da87a2edd62c06cd4357593
ms.sourcegitcommit: b6b8459eb654040f1e19f66411b29fc9e48e95c9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2020
ms.locfileid: "82030575"
---
# <a name="testing-and-debugging"></a>Teste e depuração

Como acontece com a programação clássica, é essencial ser capaz de verificar se os programas quânticos agem como pretendido, e ser capaz de diagnosticar um programa quântico que está incorreto.
Nesta seção, cobrimos as ferramentas oferecidas pelo Q# para testar e depurar programas quânticos.

## <a name="unit-tests"></a>Testes de Unidade

Uma abordagem comum para testar programas clássicos é escrever pequenos programas chamados *testes unitários* que executam código em uma biblioteca e comparar sua saída com alguma saída esperada.
Por exemplo, podemos querer `Square(2)` garantir `4`esse retorno, já que sabemos *a priori* que $2^2 = 4$.

Q# suporta a criação de testes unitários para programas quânticos, e que podem ser executados como testes dentro da estrutura de teste da unidade [xUnit.](https://xunit.github.io/)

### <a name="creating-a-test-project"></a>Criando um projeto de teste

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Abra o Visual Studio 2019. Vá para `File` o `New`  >  `Project...`menu e selecione .
No canto superior direito, procure `Q#` `Q# Test Project` e selecione o modelo.

#### <a name="command-line--visual-studio-code"></a>[Linha de comando/Visual Studio Code](#tab/tabid-vscode)

Na sua linha de comando favorita, execute o seguinte comando:
```bash
$ dotnet new xunit -lang Q# -o Tests
$ cd Tests
$ code . # To open in Visual Studio Code
```

****

Seu novo projeto terá `Tests.qs`um único arquivo, que fornece um lugar conveniente para definir novos testes de unidade Q#.
Inicialmente, este arquivo `AllocateQubit` contém um teste de unidade de amostra que{0}verifica se um qubit recém-alocado está no estado de $\ket $ e imprime uma mensagem:

```qsharp
    @Test("QuantumSimulator")
    operation AllocateQubit () : Unit {

        using (qubit = Qubit()) {
            Assert([PauliZ], [qubit], Zero, "Newly allocated qubit must be in the |0⟩ state.");
        }
        
        Message("Test passed");
    }
```

:novo: Qualquer operação Q# ou função `Unit` que `Unit` leve um argumento de tipo `@Test("...")` e retorno pode ser marcada como um teste de unidade através do atributo. O argumento para `"QuantumSimulator"` esse atributo, acima, especifica o destino no qual o teste é executado. Um único teste pode ser executado em vários alvos. Por exemplo, adicione `@Test("ResourcesEstimator")` `AllocateQubit`um atributo acima . 
```qsharp
    @Test("QuantumSimulator")
    @Test("ResourcesEstimator")
    operation AllocateQubit () : Unit {
        ...
```
Salve o arquivo e execute todos os testes. Agora devem ser realizados dois testes de unidade, um em que o AllocateQubit é executado no QuantumSimulator e outro onde ele é executado no ResourceEstimator. 

O compilador Q# reconhece os alvos incorporados "QuantumSimulator", "ToffoliSimulator" e "ResourcesEstimator" como alvos de execução válidos para testes unitários. Também é possível especificar qualquer nome totalmente qualificado para definir um alvo de execução personalizado. 

### <a name="running-q-unit-tests"></a>Executando testes de unidade Q#

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Como uma configuração única por solução, `Test` vá `Test Settings`  >  `Default Processor Architecture`  > para o menu e selecione `X64`.

> [!TIP]
> A configuração padrão da arquitetura do processador`.suo`para o Visual Studio é armazenada no arquivo de opções de solução () para cada solução.
> Se você excluir este arquivo, então `X64` você precisará selecionar como sua arquitetura de processador novamente.

Construa o projeto, `Test` vá `Windows`  >  `Test Explorer`para o menu e selecione . `AllocateQubit`aparecerão na lista de testes `Not Run Tests` no grupo. Selecione `Run All` ou execute este teste individual, e ele deve passar!

#### <a name="command-line--visual-studio-code"></a>[Linha de comando/Visual Studio Code](#tab/tabid-vscode)

Para executar os testes, navegue até `Tests.csproj`a pasta do projeto (a pasta que contém), e execute o comando:

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

Os testes unitários podem ser filtrados de acordo com seu nome e/ou o alvo de execução:

```bash 
$ dotnet test --filter "Target=QuantumSimulator"
$ dotnet test --filter "Name=AllocateQubit"
```


***

A função <xref:microsoft.quantum.intrinsic.message> intrínseca `(String -> Unit)` tem tipo e permite a criação de mensagens de diagnóstico.

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Depois de executar um teste no Test Explorer e clicar no teste, um painel aparecerá com informações sobre a execução do teste: status aprovado/falhado, tempo decorrido e um link "Saída". Se você clicar no link "Saída", a saída de teste será aberta em uma nova janela.

![saída de teste](~/media/unit-test-output.png)

#### <a name="command-line--visual-studio-code"></a>[Linha de comando/Visual Studio Code](#tab/tabid-vscode)

O status de aprovação/falha de cada `dotnet test`teste é impresso no console por .
Para testes de falha, as saídas também são impressas no console para ajudar a diagnosticar a falha.

***

## <a name="facts-and-assertions"></a>Fatos e Afirmações

Como as funções em Q# não têm efeitos _colaterais lógicos,_ quaisquer _outros tipos_ `()` de efeitos da execução de uma função cujo tipo de saída é a tupla vazia nunca podem ser observados dentro de um programa Q#.
Ou seja, uma máquina de destino pode `()` optar por não executar qualquer função que retorne com a garantia de que essa omissão não modificará o comportamento de qualquer código Q# seguinte.
Isso faz com `()` que as funções retornem (ou `Unit`seja) uma ferramenta útil para incorporar afirmações e depurar lógica em programas Q#. 

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

Aqui, a `fail` palavra-chave indica que a computação não deve prosseguir, levantando uma exceção na máquina de destino que executa o programa Q#.
Por definição, uma falha desse tipo não pode ser observada dentro de Q#, pois nenhum código Q# adicional é executado após uma `fail` declaração ser alcançada.
Assim, se passarmos por `PositivityFact`uma chamada para , podemos ter certeza de que sua contribuição foi positiva.

Observe que podemos implementar o `PositivityFact` mesmo [`Fact`](xref:microsoft.quantum.diagnostics.fact) comportamento <xref:microsoft.quantum.diagnostics> que usar a função a partir do namespace:

```qsharp
    Fact(value > 0, "Expected a positive number.");
```

*As afirmações,* por outro lado, são usadas de forma semelhante aos fatos, mas podem depender do estado da máquina alvo. Correspondentemente, são definidas como operações, enquanto os fatos são definidos como funções (como acima).
Para entender a distinção, considere o seguinte uso de um fato dentro de uma afirmação:

```qsharp
operation AssertQubitsAreAvailable() : Unit
{
     Fact(GetQubitsAvailableToUse() > 0, "No qubits were actually available");
}
```

Aqui, estamos usando <xref:microsoft.quantum.environment.getqubitsavailabletouse> a operação para retornar o número de qubits disponíveis para uso.
Como isso depende claramente do estado global do programa e `AssertQubitsAreAvailable` do seu ambiente de execução, nossa definição deve ser uma operação também.
No entanto, podemos usar esse `Bool` estado global para `Fact` produzir um valor simples como entrada para a função.

Com base nessas ideias, [o prelúdio](xref:microsoft.quantum.libraries.standard.prelude) <xref:microsoft.quantum.intrinsic.assert> oferece <xref:microsoft.quantum.intrinsic.assertprob> duas afirmações especialmente `()`úteis, e ambas modeladas como operações para . Essas afirmações tomam cada um um operador de Pauli descrevendo uma medição particular de interesse, um registro quântico no qual uma medição deve ser realizada, e um resultado hipotético.
Em máquinas-alvo que funcionam por simulação, não estamos vinculados [ao teorema da não clonagem,](https://en.wikipedia.org/wiki/No-cloning_theorem)e podemos realizar tais medições sem perturbar o registro passado a tais afirmações.
Um simulador pode, então, semelhante à função acima, abortar a `PositivityFact` computação se o resultado hipotético não for observado na prática:

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

No hardware quântico físico, onde o teorema sem clonagem `Assert` `AssertProb` impede o `()` exame do estado quântico, as operações simplesmente retornam sem outro efeito.

O <xref:microsoft.quantum.diagnostics> namespace fornece várias `Assert` outras funções da família que nos permitem verificar condições mais avançadas. 

## <a name="dump-functions"></a>Funções de despejo

Para ajudar a solucionar problemas de programas quânticos, o <xref:microsoft.quantum.diagnostics> namespace <xref:microsoft.quantum.diagnostics.dumpmachine> oferece <xref:microsoft.quantum.diagnostics.dumpregister>duas funções que podem despejar em um arquivo o status atual da máquina de destino: e . A saída gerada de cada um depende da máquina alvo.

### <a name="dumpmachine"></a>DumpMachine

O simulador quântico de estado completo distribuído como parte do Kit de Desenvolvimento Quântico escreve no arquivo a função de [onda](https://en.wikipedia.org/wiki/Wave_function) de todo o sistema quântico, como uma matriz unidimensional de números complexos, em que cada elemento representa a amplitude da probabilidade de medir o estado de base computacional $\ket{n}$, onde $\ket{n} = \ket{b_{n-1}... b_1b_0}$ por bits $\{b_i\}$. Por exemplo, em uma máquina com apenas dois qubits alocados e no estado quântico $${1}\start{align} \ket{\psi} = \frac {\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10}, \end{align} $$ a chamada <xref:microsoft.quantum.diagnostics.dumpmachine> gera essa saída:

```
# wave function for qubits with ids (least to most significant): 0;1
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣2❭:    -0.500000 + -0.500000 i  ==     **********           [ 0.500000 ]   /     [ -2.35619 rad ]
∣3❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

A primeira linha fornece um comentário com os IDs dos qubits correspondentes em sua ordem significativa.
O resto das linhas descrevem a amplitude de probabilidade de medir o vetor de estado base $\ket{n}$ em formatos cartesiano e polar. Em detalhes para a primeira linha:

* **`∣0❭:`** esta linha corresponde `0` ao estado de base computacional
* **`0.707107 +  0.000000 i`**: a amplitude de probabilidade no formato cartesiano.
* **` == `**: `equal` o sinal separa ambas as representações equivalentes.
* **`**********  `**: Uma representação gráfica da magnitude, o número de `*` é proporcional à probabilidade de medir este vetor de estado.
* **`[ 0.500000 ]`**: o valor numérico da magnitude
* **`    ---`**: Representação gráfica da fase da amplitude (veja abaixo).
* **`[ 0.0000 rad ]`**: o valor numérico da fase (em radianos).

Tanto a magnitude quanto a fase são exibidas com uma representação gráfica. A representação de magnitude é direta: `*`mostra uma barra de , quanto maior a probabilidade, maior será a barra. Para a fase, mostramos os seguintes símbolos para representar o ângulo com base em intervalos:

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

Os exemplos a `DumpMachine` seguir mostram para alguns estados comuns:

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
  > O id de um qubit é atribuído em tempo de execução e não está necessariamente alinhado com a ordem em que o qubit foi alocado ou sua posição dentro de um registro de qubit.


#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

  > [!TIP]
  > Você pode descobrir um id de qubit no Visual Studio colocando um ponto de ruptura em seu código e inspecionando o valor de uma variável de qubit, por exemplo:
  > 
  > ![mostrar id qubit no Visual Studio](~/media/qubit_id.png)
  >
  > o qubit `0` com `register2` índice em`3`has id= `1` , o`2`qubit com índice tem id= .

#### <a name="command-line--visual-studio-code"></a>[Linha de comando/Visual Studio Code](#tab/tabid-vscode)

  > [!TIP]
  > Você pode descobrir um id de <xref:microsoft.quantum.intrinsic.message> qubit usando a função e passando a variável qubit na mensagem, por exemplo:
  >
  > ```qsharp
  > Message($"0={register2[0]}; 1={register2[1]}");
  > ```
  > 
  > que poderia gerar essa saída:
  >```
  > 0=q:3; 1=q:2
  >```
  > o que significa que `0` o `register2` qubit`3`com índice ligado `1` tem id= , o qubit com índice tem id=`2`.


***

<xref:microsoft.quantum.diagnostics.dumpmachine>faz parte <xref:microsoft.quantum.diagnostics> do namespace, então para usá-lo `open` você deve adicionar uma declaração:

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

<xref:microsoft.quantum.diagnostics.dumpregister>funciona <xref:microsoft.quantum.diagnostics.dumpmachine>como , exceto que também é preciso um conjunto de qubits para limitar a quantidade de informações apenas a que é relevante para os qubits correspondentes.

Como <xref:microsoft.quantum.diagnostics.dumpmachine>acontece, as <xref:microsoft.quantum.diagnostics.dumpregister> informações geradas pela máquina alvo dependem da máquina alvo. Para o simulador quântico de estado completo, ele grava no arquivo a função de onda até uma fase global <xref:microsoft.quantum.diagnostics.dumpmachine>do subsistema quântico gerado pelos qubits fornecidos no mesmo formato que .  Por{1}exemplo, pegue novamente uma máquina com apenas dois qubits alocados e no estado quântico $$ \start{align}{2}\ket{\psi} = \frac {\sqrt } \ket{00} - \frac{(1 + i)}{2} \ket{10} = - e^{-i\pi/4 } ({1}(\frac {\sqrt{2}} \ket{0} - \frac{(1 + i)}{2} \ket{1} ) \otimes \frac{-(1 + i)}{\sqrt{2}} \ket{0} ) , \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[0]` generates this output:

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:    -0.707107 + -0.707107 i  ==     ******************** [ 1.000000 ]  /      [ -2.35619 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

e <xref:microsoft.quantum.diagnostics.dumpregister> chamar `qubit[1]` para gera essa saída:

```
# wave function for qubits with ids (least to most significant): 1
∣0❭:     0.707107 +  0.000000 i  ==     ***********          [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:    -0.500000 + -0.500000 i  ==     ***********          [ 0.500000 ]  /      [ -2.35619 rad ]
```

Em geral, o estado de um registro que está emaranhado com outro registro é um estado misto e não um estado puro. Neste caso, <xref:microsoft.quantum.diagnostics.dumpregister> produz a seguinte mensagem:

```
Qubits provided (0;) are entangled with some other qubit.
```

O exemplo a seguir mostra <xref:microsoft.quantum.diagnostics.dumpregister> como <xref:microsoft.quantum.diagnostics.dumpmachine> você pode usar ambos e em seu código Q#:

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

Além das `Assert` `Dump` funções e operações, q# suporta um subconjunto de recursos padrão de depuração visual Studio: definir pontos de interrupção de [linha,](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints) [passar pelo código usando F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) e [inspecionar valores de variáveis clássicas](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) são todos possíveis durante a execução de código no simulador.

A depuração no Visual Studio Code aproveita os recursos de depuração fornecidos pela extensão C# for Visual Studio Code alimentada pelo OmniSharp e requer a instalação da [versão mais recente](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp). 
