---
title: Testando e depurando
description: Saiba como usar testes de unidade, fatos e asserções e funções de despejo para testar e depurar programas Quantum.
author: tcNickolas
ms.author: mamykhai
ms.date: 06/01/2020
ms.topic: article
uid: microsoft.quantum.guide.testingdebugging
no-loc:
- 'Q#'
- '$$v'
ms.openlocfilehash: 5505086c5efac89f6940cde1ecae2ce629cfeda5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92690964"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="ab324-103">Testando e depurando</span><span class="sxs-lookup"><span data-stu-id="ab324-103">Testing and debugging</span></span>

<span data-ttu-id="ab324-104">Assim como acontece com a programação clássica, é essencial poder verificar se os programas Quantum atuam como pretendidos e podem diagnosticar o comportamento incorreto.</span><span class="sxs-lookup"><span data-stu-id="ab324-104">As with classical programming, it is essential to be able to check that quantum programs act as intended, and to be able to diagnose incorrect behavior.</span></span>
<span data-ttu-id="ab324-105">Nesta seção, abordaremos as ferramentas oferecidas pelo Q# para testar e depurar programas Quantum.</span><span class="sxs-lookup"><span data-stu-id="ab324-105">In this section, we cover the tools offered by Q# for testing and debugging quantum programs.</span></span>

## <a name="unit-tests"></a><span data-ttu-id="ab324-106">Testes de Unidade</span><span class="sxs-lookup"><span data-stu-id="ab324-106">Unit Tests</span></span>

<span data-ttu-id="ab324-107">Uma abordagem comum para testar programas clássicos é escrever programas pequenos chamados de *testes de unidade* , que executam o código em uma biblioteca e comparam sua saída a alguma saída esperada.</span><span class="sxs-lookup"><span data-stu-id="ab324-107">One common approach to testing classical programs is to write small programs called *unit tests* , which run code in a library and compare its output to some expected output.</span></span>
<span data-ttu-id="ab324-108">Por exemplo, você pode garantir que os `Square(2)` retornos `4` desde que você saiba *um priori* que $2 ^ 2 = $4.</span><span class="sxs-lookup"><span data-stu-id="ab324-108">For example, you can ensure that `Square(2)` returns `4` since you know *a priori* that $2^2 = 4$.</span></span>

<span data-ttu-id="ab324-109">Q# dá suporte à criação de testes de unidade para programas Quantum e que podem ser executados como testes dentro da estrutura de teste de unidade do [xUnit](https://xunit.github.io/) .</span><span class="sxs-lookup"><span data-stu-id="ab324-109">Q# supports creating unit tests for quantum programs, and which can run as tests within the [xUnit](https://xunit.github.io/) unit testing framework.</span></span>

### <a name="creating-a-test-project"></a><span data-ttu-id="ab324-110">Criando um projeto de teste</span><span class="sxs-lookup"><span data-stu-id="ab324-110">Creating a Test Project</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="ab324-111">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="ab324-111">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="ab324-112">Abra o Visual Studio 2019.</span><span class="sxs-lookup"><span data-stu-id="ab324-112">Open Visual Studio 2019.</span></span> <span data-ttu-id="ab324-113">Vá para o menu **arquivo** e selecione **novo > projeto...** . No canto superior direito, procure `Q#` e selecione o modelo projeto de **Q# teste** .</span><span class="sxs-lookup"><span data-stu-id="ab324-113">Go to the **File** menu and select **New > Project...** . In the upper right corner, search for `Q#`, and select the **Q# Test Project** template.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="ab324-114">Linha de comando/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="ab324-114">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="ab324-115">Na sua linha de comando favorita, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="ab324-115">From your favorite command line, run the following command:</span></span>
```dotnetcli
$ dotnet new xunit -lang Q# -o Tests
$ cd Tests
$ code . # To open in Visual Studio Code
```

****

<span data-ttu-id="ab324-116">Seu novo projeto tem um único arquivo `Tests.qs` , que fornece um local conveniente para definir novos Q# testes de unidade.</span><span class="sxs-lookup"><span data-stu-id="ab324-116">Your new project has a single file `Tests.qs`, which provides a convenient place to define new Q# unit tests.</span></span>
<span data-ttu-id="ab324-117">Inicialmente, esse arquivo contém um teste de unidade de exemplo `AllocateQubit` que verifica se um qubit alocado recentemente está no estado $ \ket {0} $ e imprime uma mensagem:</span><span class="sxs-lookup"><span data-stu-id="ab324-117">Initially, this file contains one sample unit test `AllocateQubit` which checks that a newly allocated qubit is in the $\ket{0}$ state and prints a message:</span></span>

```qsharp
    @Test("QuantumSimulator")
    operation AllocateQubit () : Unit {

        using (qubit = Qubit()) {
            AssertMeasurement([PauliZ], [qubit], Zero, "Newly allocated qubit must be in the |0⟩ state.");
        }
        
        Message("Test passed");
    }
```

<span data-ttu-id="ab324-118">Qualquer Q# operação ou função que usa um argumento de tipo `Unit` e retornos `Unit` pode ser marcada como um teste de unidade por meio do `@Test("...")` atributo.</span><span class="sxs-lookup"><span data-stu-id="ab324-118">Any Q# operation or function that takes an argument of type `Unit` and returns `Unit` can be marked as a unit test via the `@Test("...")` attribute.</span></span> <span data-ttu-id="ab324-119">No exemplo anterior, o argumento para esse atributo, `"QuantumSimulator"` , especifica o destino no qual o teste é executado.</span><span class="sxs-lookup"><span data-stu-id="ab324-119">In the previous example, the argument to that attribute, `"QuantumSimulator"`, specifies the target on which the test runs.</span></span> <span data-ttu-id="ab324-120">Um único teste pode ser executado em vários destinos.</span><span class="sxs-lookup"><span data-stu-id="ab324-120">A single test can run on multiple targets.</span></span> <span data-ttu-id="ab324-121">Por exemplo, adicione um atributo `@Test("ResourcesEstimator")` antes de `AllocateQubit` .</span><span class="sxs-lookup"><span data-stu-id="ab324-121">For example, add an attribute `@Test("ResourcesEstimator")` before `AllocateQubit`.</span></span> 
```qsharp
    @Test("QuantumSimulator")
    @Test("ResourcesEstimator")
    operation AllocateQubit () : Unit {
        ...
```
<span data-ttu-id="ab324-122">Salve o arquivo e execute todos os testes.</span><span class="sxs-lookup"><span data-stu-id="ab324-122">Save the file and run all tests.</span></span> <span data-ttu-id="ab324-123">Agora deve haver dois testes de unidade, um em que `AllocateQubit` é executado no `QuantumSimulator` e um onde ele é executado no `ResourcesEstimator` .</span><span class="sxs-lookup"><span data-stu-id="ab324-123">There should now be two unit tests, one where `AllocateQubit` runs on the `QuantumSimulator`, and one where it runs in the `ResourcesEstimator`.</span></span> 

<span data-ttu-id="ab324-124">O Q# compilador reconhece os destinos internos `"QuantumSimulator"` , `"ToffoliSimulator"` e `"ResourcesEstimator"` como destinos de execução válidos para testes de unidade.</span><span class="sxs-lookup"><span data-stu-id="ab324-124">The Q# compiler recognizes the built-in targets `"QuantumSimulator"`, `"ToffoliSimulator"`, and `"ResourcesEstimator"` as valid run targets for unit tests.</span></span> <span data-ttu-id="ab324-125">Também é possível especificar qualquer nome totalmente qualificado para definir um destino de execução personalizado.</span><span class="sxs-lookup"><span data-stu-id="ab324-125">It is also possible to specify any fully qualified name to define a custom run target.</span></span> 

### <a name="running-no-locq-unit-tests"></a><span data-ttu-id="ab324-126">Executando Q# testes de unidade</span><span class="sxs-lookup"><span data-stu-id="ab324-126">Running Q# Unit Tests</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="ab324-127">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="ab324-127">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="ab324-128">Como configuração única por solução, vá para o menu **teste** e selecione **configurações de teste > arquitetura de processador padrão > x64** .</span><span class="sxs-lookup"><span data-stu-id="ab324-128">As a one-time per-solution setup, go to the **Test** menu and select **Test Settings > Default Processor Architecture > X64** .</span></span>

> [!TIP]
> <span data-ttu-id="ab324-129">A configuração de arquitetura de processador padrão para o Visual Studio é armazenada no `.suo` arquivo de opções de solução () para cada solução.</span><span class="sxs-lookup"><span data-stu-id="ab324-129">The default processor architecture setting for Visual Studio is stored in the solution options (`.suo`) file for each solution.</span></span>
> <span data-ttu-id="ab324-130">Se você excluir esse arquivo, precisará selecionar **x64** como a arquitetura do processador novamente.</span><span class="sxs-lookup"><span data-stu-id="ab324-130">If you delete this file, then you need to select **X64** as your processor architecture again.</span></span>

<span data-ttu-id="ab324-131">Crie o projeto, abra o menu **testar** e selecione **Windows > Test Explorer** .</span><span class="sxs-lookup"><span data-stu-id="ab324-131">Build the project, open the **Test** menu, and select **Windows > Test Explorer** .</span></span> <span data-ttu-id="ab324-132">**AllocateQubit** é exibido na lista de testes no grupo de **testes não executado** .</span><span class="sxs-lookup"><span data-stu-id="ab324-132">**AllocateQubit** displays in the list of tests in the **Not Run Tests** group.</span></span> <span data-ttu-id="ab324-133">Selecione **executar tudo** ou executar este teste individual.</span><span class="sxs-lookup"><span data-stu-id="ab324-133">Select **Run All** or run this individual test.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="ab324-134">Linha de comando/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="ab324-134">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="ab324-135">Para executar testes, navegue até a pasta do projeto (a pasta que contém `Tests.csproj` ) e execute o comando:</span><span class="sxs-lookup"><span data-stu-id="ab324-135">To run tests, navigate to the project folder (the folder which contains `Tests.csproj`), and run the command:</span></span>

```bash
$ dotnet restore
$ dotnet test
```

<span data-ttu-id="ab324-136">Você deve ver um resultado semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="ab324-136">You should get output similar to the following:</span></span>

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

<span data-ttu-id="ab324-137">Os testes de unidade podem ser filtrados de acordo com seu nome ou o destino de execução:</span><span class="sxs-lookup"><span data-stu-id="ab324-137">Unit tests can be filtered according to their name or the run target:</span></span>

```bash 
$ dotnet test --filter "Target=QuantumSimulator"
$ dotnet test --filter "Name=AllocateQubit"
```


<span data-ttu-id="ab324-138">\*\*_</span><span class="sxs-lookup"><span data-stu-id="ab324-138">\*\*_</span></span>

<span data-ttu-id="ab324-139">A função intrínseca <xref:Microsoft.Quantum.Intrinsic.Message> tem o tipo `(String -> Unit)` e habilita a criação de mensagens de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="ab324-139">The intrinsic function <xref:Microsoft.Quantum.Intrinsic.Message> has type `(String -> Unit)` and enables the creation of diagnostic messages.</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="ab324-140">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="ab324-140">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="ab324-141">Depois de executar um teste no Test Explorer e clicar no teste, um painel será exibido com informações sobre a execução de teste: status de aprovação/falha, tempo decorrido e um link para a saída.</span><span class="sxs-lookup"><span data-stu-id="ab324-141">After you run a test in Test Explorer and click on the test, a panel displays with information about test run: Pass/fail status, elapsed time, and a link to the output.</span></span> <span data-ttu-id="ab324-142">Clique em _ *output* \* para abrir a saída de teste em uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="ab324-142">Click _ *Output* \* to open the test output in a new window.</span></span>

![saída de teste](~/media/unit-test-output.png)

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="ab324-144">Linha de comando/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="ab324-144">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="ab324-145">O status de aprovação/reprovação de cada teste é impresso no console do `dotnet test` .</span><span class="sxs-lookup"><span data-stu-id="ab324-145">The pass/fail status for each test is printed to the console by `dotnet test`.</span></span>
<span data-ttu-id="ab324-146">Para testes com falha, as saídas também são impressas no console do para ajudar a diagnosticar a falha.</span><span class="sxs-lookup"><span data-stu-id="ab324-146">For failing tests, the outputs are also printed to the console to help diagnose the failure.</span></span>

<span data-ttu-id="ab324-147">\*\*_</span><span class="sxs-lookup"><span data-stu-id="ab324-147">\*\*_</span></span>

## <a name="facts-and-assertions"></a><span data-ttu-id="ab324-148">Fatos e asserções</span><span class="sxs-lookup"><span data-stu-id="ab324-148">Facts and Assertions</span></span>

<span data-ttu-id="ab324-149">Como as funções no Q# não têm efeitos colaterais _lógicos_ , você nunca pode observar, de dentro de um Q# programa, quaisquer outros tipos de efeitos da execução de uma função cujo tipo de saída seja a tupla vazia `()` .</span><span class="sxs-lookup"><span data-stu-id="ab324-149">Because functions in Q# have no _logical_ side effects, you can never observe, from within a Q# program, any other kinds of effects from running a function whose output type is the empty tuple `()`.</span></span>
<span data-ttu-id="ab324-150">Ou seja, um computador de destino pode optar por não executar nenhuma função que retorna `()` com a garantia de que essa omissão não modificará o comportamento de qualquer código a seguir Q# .</span><span class="sxs-lookup"><span data-stu-id="ab324-150">That is, a target machine can choose not to run any function which returns `()` with the guarantee that this omission will not modify the behavior of any following Q# code.</span></span>
<span data-ttu-id="ab324-151">Esse comportamento faz com que as funções retornem `()` (como `Unit` ) uma ferramenta útil para incorporar asserções e depurar a lógica em Q# programas.</span><span class="sxs-lookup"><span data-stu-id="ab324-151">This behavior makes functions returning `()` (such as `Unit`) a useful tool for embedding assertions and debugging logic into Q# programs.</span></span> 

<span data-ttu-id="ab324-152">Vamos considerar um exemplo simples:</span><span class="sxs-lookup"><span data-stu-id="ab324-152">Let's consider a simple example:</span></span>

```qsharp
function PositivityFact(value : Double) : Unit 
{
    if (value <= 0) 
    {
        fail "Expected a positive number.";
    }
}
```

<span data-ttu-id="ab324-153">Aqui, a palavra-chave `fail` indica que a computação não deve continuar e gera uma exceção no computador de destino que executa o Q# programa.</span><span class="sxs-lookup"><span data-stu-id="ab324-153">Here, the keyword `fail` indicates that the computation should not proceed, and raises an exception in the target machine running the Q# program.</span></span>
<span data-ttu-id="ab324-154">Por definição, uma falha desse tipo não pode ser observada de dentro do Q# , pois o computador de destino não executa mais o Q# código depois de atingir uma `fail` instrução.</span><span class="sxs-lookup"><span data-stu-id="ab324-154">By definition, a failure of this kind cannot be observed from within Q#, as the target machine no longer runs the Q# code after reaching a `fail` statement.</span></span>
<span data-ttu-id="ab324-155">Portanto, se continuarmos após uma chamada para `PositivityFact` , poderemos ter certeza de que sua entrada foi positiva.</span><span class="sxs-lookup"><span data-stu-id="ab324-155">Thus, if we proceed past a call to `PositivityFact`, we can be assured that its input was positive.</span></span>

<span data-ttu-id="ab324-156">Observe que podemos implementar o mesmo comportamento que `PositivityFact` usar a [`Fact`](xref:Microsoft.Quantum.Diagnostics.fact) função do <xref:Microsoft.Quantum.Diagnostics> namespace:</span><span class="sxs-lookup"><span data-stu-id="ab324-156">Note that we can implement the same behavior as `PositivityFact` using the [`Fact`](xref:Microsoft.Quantum.Diagnostics.fact) function from the <xref:Microsoft.Quantum.Diagnostics> namespace:</span></span>

```qsharp
    Fact(value > 0, "Expected a positive number.");
```

<span data-ttu-id="ab324-157">_Assertions \*, por outro lado, é usado da mesma forma para os fatos, mas pode depender do estado do computador de destino.</span><span class="sxs-lookup"><span data-stu-id="ab324-157">_Assertions\*, on the other hand, are used similarly to facts but may depend on the state of the target machine.</span></span> <span data-ttu-id="ab324-158">De forma correspondente, eles são definidos como operações, enquanto os fatos são definidos como funções (como no exemplo anterior).</span><span class="sxs-lookup"><span data-stu-id="ab324-158">Correspondingly, they are defined as operations, whereas facts are defined as functions (as in the previous example).</span></span>
<span data-ttu-id="ab324-159">Para entender a distinção, considere o seguinte uso de um fato em uma asserção:</span><span class="sxs-lookup"><span data-stu-id="ab324-159">To understand the distinction, consider the following use of a fact within an assertion:</span></span>

```qsharp
operation AssertQubitsAreAvailable() : Unit
{
     Fact(GetQubitsAvailableToUse() > 0, "No qubits were actually available");
}
```

<span data-ttu-id="ab324-160">Aqui, estamos usando a operação <xref:Microsoft.Quantum.Environment.GetQubitsAvailableToUse> para retornar o número de qubits disponíveis para uso.</span><span class="sxs-lookup"><span data-stu-id="ab324-160">Here, we are using the operation <xref:Microsoft.Quantum.Environment.GetQubitsAvailableToUse> to return the number of qubits available to use.</span></span>
<span data-ttu-id="ab324-161">Como isso depende do estado global do programa e de seu ambiente de execução, nossa definição de `AssertQubitsAreAvailable` deve ser uma operação também.</span><span class="sxs-lookup"><span data-stu-id="ab324-161">As this depends on the global state of the program and its run environment, our definition of `AssertQubitsAreAvailable` must be an operation as well.</span></span>
<span data-ttu-id="ab324-162">No entanto, podemos usar esse estado global para gerar um `Bool` valor simples como entrada para a `Fact` função.</span><span class="sxs-lookup"><span data-stu-id="ab324-162">However, we can use that global state to yield a simple `Bool` value as input to the `Fact` function.</span></span>

<span data-ttu-id="ab324-163">[A prelúdio, a](xref:microsoft.quantum.libraries.standard.prelude)criação dessas ideias, oferece duas declarações especialmente úteis <xref:Microsoft.Quantum.Diagnostics.AssertMeasurement> e <xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability> modeladas como operações no `()` .</span><span class="sxs-lookup"><span data-stu-id="ab324-163">[The prelude](xref:microsoft.quantum.libraries.standard.prelude), building on these ideas, offers two especially useful assertions, <xref:Microsoft.Quantum.Diagnostics.AssertMeasurement> and <xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability> both modeled as operations onto `()`.</span></span> <span data-ttu-id="ab324-164">Essas asserções adotam um operador Pauli que descreve uma medição específica de interesse, um registro Quantum no qual uma medida é executada e um resultado hipotético.</span><span class="sxs-lookup"><span data-stu-id="ab324-164">These assertions each take a Pauli operator describing a particular measurement of interest, a quantum register on which a measurement is performed, and a hypothetical outcome.</span></span>
<span data-ttu-id="ab324-165">Os computadores de destino que trabalham por simulação não são vinculados pelo [teorema no-Cloning](https://en.wikipedia.org/wiki/No-cloning_theorem)e podem executar essas medições sem perturbar o registro que passa para tais asserções.</span><span class="sxs-lookup"><span data-stu-id="ab324-165">Target machines which work by simulation are not bound by [the no-cloning theorem](https://en.wikipedia.org/wiki/No-cloning_theorem), and can perform such measurements without disturbing the register that passes to such assertions.</span></span>
<span data-ttu-id="ab324-166">Um simulador pode, assim, semelhante à `PositivityFact` função anterior, interromper a computação se o resultado hipotético não for observado na prática:</span><span class="sxs-lookup"><span data-stu-id="ab324-166">A simulator can then, similar to the `PositivityFact` function previous, stop computation if the hypothetical outcome is not observed in practice:</span></span>

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

<span data-ttu-id="ab324-167">Em hardware Quantum físico, em que o teorema no-Cloning impede o exame de um estado Quantum, as `AssertMeasurement` `AssertMeasurementProbability` operações e simplesmente retornam `()` sem nenhum outro efeito.</span><span class="sxs-lookup"><span data-stu-id="ab324-167">On physical quantum hardware, where the no-cloning theorem prevents examination of a quantum state, the `AssertMeasurement` and `AssertMeasurementProbability` operations simply return `()` with no other effect.</span></span>

<span data-ttu-id="ab324-168">O <xref:Microsoft.Quantum.Diagnostics> namespace fornece várias outras funções da `Assert` família, com as quais você pode verificar condições mais avançadas.</span><span class="sxs-lookup"><span data-stu-id="ab324-168">The <xref:Microsoft.Quantum.Diagnostics> namespace provides several more functions of the `Assert` family, with which you can check more advanced conditions.</span></span> 

## <a name="dump-functions"></a><span data-ttu-id="ab324-169">Funções de despejo</span><span class="sxs-lookup"><span data-stu-id="ab324-169">Dump Functions</span></span>

<span data-ttu-id="ab324-170">Para ajudar a solucionar problemas de programas Quantum, o <xref:Microsoft.Quantum.Diagnostics> namespace oferece duas funções que podem ser despejadas em um arquivo o status atual do computador de destino: <xref:Microsoft.Quantum.Diagnostics.DumpMachine> e <xref:Microsoft.Quantum.Diagnostics.DumpRegister> .</span><span class="sxs-lookup"><span data-stu-id="ab324-170">To help troubleshooting quantum programs, the <xref:Microsoft.Quantum.Diagnostics> namespace offers two functions that can dump into a file the current status of the target machine: <xref:Microsoft.Quantum.Diagnostics.DumpMachine> and <xref:Microsoft.Quantum.Diagnostics.DumpRegister>.</span></span> <span data-ttu-id="ab324-171">A saída gerada de cada uma depende do computador de destino.</span><span class="sxs-lookup"><span data-stu-id="ab324-171">The generated output of each depends on the target machine.</span></span>

### <a name="dumpmachine"></a><span data-ttu-id="ab324-172">DumpMachine</span><span class="sxs-lookup"><span data-stu-id="ab324-172">DumpMachine</span></span>

<span data-ttu-id="ab324-173">O simulador de Quantum completo distribuído como parte do kit de desenvolvimento Quantum grava no arquivo a [função de onda](https://en.wikipedia.org/wiki/Wave_function) de todo o sistema Quantum, como uma matriz unidimensional de números complexos, na qual cada elemento representa a amplitude da probabilidade de medir o estado de base computacional $ \ket{n} $, em que $ \ket{n} = \ket{b_ {n-1}... b_1b_0} $ para bits $ \{ b_i \} $.</span><span class="sxs-lookup"><span data-stu-id="ab324-173">The full-state quantum simulator distributed as part of the Quantum Development Kit writes into the file the [wave function](https://en.wikipedia.org/wiki/Wave_function) of the entire quantum system, as a one-dimensional array of complex numbers, in which each element represents the amplitude of the probability of measuring the computational basis state $\ket{n}$, where $\ket{n} = \ket{b_{n-1}...b_1b_0}$ for bits $\{b_i\}$.</span></span> <span data-ttu-id="ab324-174">Por exemplo, em um computador com apenas dois qubits alocados e no estado Quantum $ $ \begin{align} \ket{\psi} = \frac {1} {\sqrt {2} } \ket {00} -\frac{(1 + i)} {2} \ket {10} , \end{align} $ $ Calling <xref:Microsoft.Quantum.Diagnostics.DumpMachine> gera essa saída:</span><span class="sxs-lookup"><span data-stu-id="ab324-174">For example, on a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10}, \end{align} $$ calling <xref:Microsoft.Quantum.Diagnostics.DumpMachine> generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0;1
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣2❭:    -0.500000 + -0.500000 i  ==     **********           [ 0.500000 ]   /     [ -2.35619 rad ]
∣3❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="ab324-175">A primeira linha fornece um comentário com as IDs do qubits correspondente em sua ordem significativa.</span><span class="sxs-lookup"><span data-stu-id="ab324-175">The first row provides a comment with the ids of the corresponding qubits in their significant order.</span></span>
<span data-ttu-id="ab324-176">O restante das linhas descreve a amplitude de probabilidade de medir o vetor de estado base $ \ket{n} $ nos formatos cartesianas e polar.</span><span class="sxs-lookup"><span data-stu-id="ab324-176">The rest of the rows describe the probability amplitude of measuring the basis state vector $\ket{n}$ in both Cartesian and polar formats.</span></span> <span data-ttu-id="ab324-177">Em detalhes para a primeira linha:</span><span class="sxs-lookup"><span data-stu-id="ab324-177">In detail for the first row:</span></span>

* <span data-ttu-id="ab324-178">**`∣0❭:`** Esta linha corresponde ao `0` estado de base computacional</span><span class="sxs-lookup"><span data-stu-id="ab324-178">**`∣0❭:`** this row corresponds to the `0` computational basis state</span></span>
* <span data-ttu-id="ab324-179">**`0.707107 +  0.000000 i`** : a amplitude de probabilidade no formato cartesiano.</span><span class="sxs-lookup"><span data-stu-id="ab324-179">**`0.707107 +  0.000000 i`** : the probability amplitude in Cartesian format.</span></span>
* <span data-ttu-id="ab324-180">**` == `** : o `equal` sinal separa as representações equivalentes.</span><span class="sxs-lookup"><span data-stu-id="ab324-180">**` == `** : the `equal` sign separates both equivalent representations.</span></span>
* <span data-ttu-id="ab324-181">**`**********  `** : Uma representação gráfica da magnitude, o número de `*` é proporcional à probabilidade de medir esse vetor de estado.</span><span class="sxs-lookup"><span data-stu-id="ab324-181">**`**********  `** : A graphical representation of the magnitude, the number of `*` is proportionate to the probability of measuring this state vector.</span></span>
* <span data-ttu-id="ab324-182">**`[ 0.500000 ]`** : o valor numérico da magnitude</span><span class="sxs-lookup"><span data-stu-id="ab324-182">**`[ 0.500000 ]`** : the numeric value of the magnitude</span></span>
* <span data-ttu-id="ab324-183">**`    ---`** : Uma representação gráfica da fase da amplitude (consulte a saída a seguir).</span><span class="sxs-lookup"><span data-stu-id="ab324-183">**`    ---`** : A graphical representation of the amplitude's phase (see the following output).</span></span>
* <span data-ttu-id="ab324-184">**`[ 0.0000 rad ]`** : o valor numérico da fase (em radianos).</span><span class="sxs-lookup"><span data-stu-id="ab324-184">**`[ 0.0000 rad ]`** : the numeric value of the phase (in radians).</span></span>

<span data-ttu-id="ab324-185">A magnitude e a fase são exibidas com uma representação gráfica.</span><span class="sxs-lookup"><span data-stu-id="ab324-185">Both the magnitude and the phase are displayed with a graphical representation.</span></span> <span data-ttu-id="ab324-186">A representação de magnitude é direta: ela mostra uma barra de `*` , quanto maior a probabilidade, maior será o tamanho da barra.</span><span class="sxs-lookup"><span data-stu-id="ab324-186">The magnitude representation is straight-forward: it shows a bar of `*`, the bigger the probability the bigger the bar will be.</span></span> <span data-ttu-id="ab324-187">Para a fase, mostramos os seguintes símbolos para representar o ângulo com base em intervalos:</span><span class="sxs-lookup"><span data-stu-id="ab324-187">For the phase, we show the following symbols to represent the angle based on ranges:</span></span>

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

<span data-ttu-id="ab324-188">Os exemplos a seguir mostram `DumpMachine` alguns Estados comuns:</span><span class="sxs-lookup"><span data-stu-id="ab324-188">The following examples show `DumpMachine` for some common states:</span></span>

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
  > <span data-ttu-id="ab324-189">A ID de um qubit é atribuída em tempo de execução e não é necessariamente alinhada com a ordem na qual o qubit foi alocado ou sua posição em um registro qubit.</span><span class="sxs-lookup"><span data-stu-id="ab324-189">The id of a qubit is assigned at runtime and is not necessarily aligned with the order in which the qubit was allocated or its position within a qubit register.</span></span>


#### <a name="visual-studio-2019"></a>[<span data-ttu-id="ab324-190">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="ab324-190">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

  > [!TIP]
  > <span data-ttu-id="ab324-191">Você pode localizar uma ID de qubit no Visual Studio colocando um ponto de interrupção em seu código e inspecionando o valor de uma variável qubit, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="ab324-191">You can locate a qubit id in Visual Studio by putting a breakpoint in your code and inspecting the value of a qubit variable, for example:</span></span>
  > 
  > ![Mostrar ID do qubit no Visual Studio](~/media/qubit_id.png)
  >
  > <span data-ttu-id="ab324-193">o qubit com índice `0` em `register2` tem ID = `3` , o qubit com índice `1` tem ID = `2` .</span><span class="sxs-lookup"><span data-stu-id="ab324-193">the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="ab324-194">Linha de comando/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="ab324-194">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

  > [!TIP]
  > <span data-ttu-id="ab324-195">Você pode localizar uma ID de qubit usando a <xref:Microsoft.Quantum.Intrinsic.Message> função e passando a variável qubit na mensagem, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="ab324-195">You can locate a qubit id by using the <xref:Microsoft.Quantum.Intrinsic.Message> function and passing the qubit variable in the message, for example:</span></span>
  >
  > ```qsharp
  > Message($"0={register2[0]}; 1={register2[1]}");
  > ```
  > 
  > <span data-ttu-id="ab324-196">que pode gerar essa saída:</span><span class="sxs-lookup"><span data-stu-id="ab324-196">which could generate this output:</span></span>
  >```
  > 0=q:3; 1=q:2
  >```
  > <span data-ttu-id="ab324-197">Isso significa que o qubit com índice `0` em `register2` tem ID = `3` , o qubit com índice `1` tem a ID = `2` .</span><span class="sxs-lookup"><span data-stu-id="ab324-197">which means that the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>


<span data-ttu-id="ab324-198">\*\*_</span><span class="sxs-lookup"><span data-stu-id="ab324-198">\*\*_</span></span>

<span data-ttu-id="ab324-199">Como <xref:Microsoft.Quantum.Diagnostics.DumpMachine> o é parte do  <xref:Microsoft.Quantum.Diagnostics> namespace, você deve adicionar uma `open` instrução para acessá-lo:</span><span class="sxs-lookup"><span data-stu-id="ab324-199">Since <xref:Microsoft.Quantum.Diagnostics.DumpMachine> is part of the  <xref:Microsoft.Quantum.Diagnostics> namespace, you must add an `open` statement to access it:</span></span>

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


### <a name="dumpregister"></a><span data-ttu-id="ab324-200">DumpRegister</span><span class="sxs-lookup"><span data-stu-id="ab324-200">DumpRegister</span></span>

<span data-ttu-id="ab324-201"><xref:Microsoft.Quantum.Diagnostics.DumpRegister> funciona como <xref:Microsoft.Quantum.Diagnostics.DumpMachine> , exceto pelo fato de que ele também usa uma matriz de qubits para limitar a quantidade de informações apenas às relevantes para o qubits correspondente.</span><span class="sxs-lookup"><span data-stu-id="ab324-201"><xref:Microsoft.Quantum.Diagnostics.DumpRegister> works like <xref:Microsoft.Quantum.Diagnostics.DumpMachine>, except that it also takes an array of qubits to limit the amount of information to only that relevant to the corresponding qubits.</span></span>

<span data-ttu-id="ab324-202">Assim como acontece com <xref:Microsoft.Quantum.Diagnostics.DumpMachine> , as informações geradas <xref:Microsoft.Quantum.Diagnostics.DumpRegister> dependem do computador de destino.</span><span class="sxs-lookup"><span data-stu-id="ab324-202">As with <xref:Microsoft.Quantum.Diagnostics.DumpMachine>, the information generated by <xref:Microsoft.Quantum.Diagnostics.DumpRegister> depends on the target machine.</span></span> <span data-ttu-id="ab324-203">Para o simulador de Quantum de estado completo, ele grava no arquivo a função de onda até uma fase global do subsistema Quantum gerado pelo qubits fornecido no mesmo formato que <xref:Microsoft.Quantum.Diagnostics.DumpMachine> .</span><span class="sxs-lookup"><span data-stu-id="ab324-203">For the full-state quantum simulator it writes into the file the wave function up to a global phase of the quantum sub-system generated by the provided qubits in the same format as <xref:Microsoft.Quantum.Diagnostics.DumpMachine>.</span></span>  <span data-ttu-id="ab324-204">Por exemplo, pegue novamente um computador com apenas dois qubits alocados e no estado Quantum $ $ \begin{align} \ket{\psi} = \frac {1} {\sqrt {2} } \ket {00} -\frac{(1 + i)} {2} \ket {10} =-e ^ {-i \ pi/4} ((\frac {1} {\sqrt {2} } \ket {0} -\frac{(1 + i)} {2} \ket {1} ) \otimes \frac{-(1 + i)} {\sqrt {2} } \ket {0} ), \end{align} $ $ chamando <xref:Microsoft.Quantum.Diagnostics.DumpRegister> para `qubit[0]` gera esta saída:</span><span class="sxs-lookup"><span data-stu-id="ab324-204">For example, take again a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10} = - e^{-i\pi/4} ( (\frac{1}{\sqrt{2}} \ket{0} - \frac{(1 + i)}{2} \ket{1} ) \otimes \frac{-(1 + i)}{\sqrt{2}} \ket{0} ) , \end{align} $$ calling <xref:Microsoft.Quantum.Diagnostics.DumpRegister> for `qubit[0]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:    -0.707107 + -0.707107 i  ==     _******************* [ 1.000000 ]  /      [ -2.35619 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="ab324-205">e chamar <xref:Microsoft.Quantum.Diagnostics.DumpRegister> for `qubit[1]` gera essa saída:</span><span class="sxs-lookup"><span data-stu-id="ab324-205">and calling <xref:Microsoft.Quantum.Diagnostics.DumpRegister> for `qubit[1]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 1
∣0❭:     0.707107 +  0.000000 i  ==     ***********          [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:    -0.500000 + -0.500000 i  ==     ***********          [ 0.500000 ]  /      [ -2.35619 rad ]
```

<span data-ttu-id="ab324-206">Em geral, o estado de um registro que é confusas com outro registro é um estado misto em vez de um estado puro.</span><span class="sxs-lookup"><span data-stu-id="ab324-206">In general, the state of a register that is entangled with another register is a mixed state rather than a pure state.</span></span> <span data-ttu-id="ab324-207">Nesse caso, <xref:Microsoft.Quantum.Diagnostics.DumpRegister> o gera a seguinte mensagem:</span><span class="sxs-lookup"><span data-stu-id="ab324-207">In this case, <xref:Microsoft.Quantum.Diagnostics.DumpRegister> outputs the following message:</span></span>

```
Qubits provided (0;) are entangled with some other qubit.
```

<span data-ttu-id="ab324-208">O exemplo a seguir mostra como você pode usar o <xref:Microsoft.Quantum.Diagnostics.DumpRegister> e <xref:Microsoft.Quantum.Diagnostics.DumpMachine> o em seu Q# código:</span><span class="sxs-lookup"><span data-stu-id="ab324-208">The following example shows you how you can use both <xref:Microsoft.Quantum.Diagnostics.DumpRegister> and <xref:Microsoft.Quantum.Diagnostics.DumpMachine> in your Q# code:</span></span>

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

## <a name="debugging"></a><span data-ttu-id="ab324-209">Depuração</span><span class="sxs-lookup"><span data-stu-id="ab324-209">Debugging</span></span>

<span data-ttu-id="ab324-210">Além de `Assert` funções e `Dump` operações, Q# o dá suporte a um subconjunto de recursos de depuração padrão do Visual Studio: [definir pontos de interrupção de linha](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), percorrer [código usando F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger)e [inspecionar valores de variáveis clássicas](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) é possível ao executar seu código no simulador.</span><span class="sxs-lookup"><span data-stu-id="ab324-210">On top of `Assert` and `Dump` functions and operations, Q# supports a subset of standard Visual Studio debugging capabilities: [setting line breakpoints](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), [stepping through code using F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger), and [inspecting values of classic variables](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) are all possible when running your code on the simulator.</span></span>

<span data-ttu-id="ab324-211">A depuração no Visual Studio Code aproveita os recursos de depuração fornecidos pelo C# para Visual Studio Code extensão da plataforma OmniSharp e requer a instalação da [versão mais recente](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp).</span><span class="sxs-lookup"><span data-stu-id="ab324-211">Debugging in Visual Studio Code leverages the debugging capabilities provided by the C# for Visual Studio Code extension powered by OmniSharp and requires installing the [latest version](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp).</span></span> 
