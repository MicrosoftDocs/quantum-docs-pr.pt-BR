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
# <a name="testing-and-debugging"></a><span data-ttu-id="03e76-103">Teste e depuração</span><span class="sxs-lookup"><span data-stu-id="03e76-103">Testing and Debugging</span></span>

<span data-ttu-id="03e76-104">Como acontece com a programação clássica, é essencial ser capaz de verificar se os programas quânticos agem como pretendido, e ser capaz de diagnosticar um programa quântico que está incorreto.</span><span class="sxs-lookup"><span data-stu-id="03e76-104">As with classical programming, it is essential to be able to check that quantum programs act as intended, and to be able to diagnose a quantum program that is incorrect.</span></span>
<span data-ttu-id="03e76-105">Nesta seção, cobrimos as ferramentas oferecidas pelo Q# para testar e depurar programas quânticos.</span><span class="sxs-lookup"><span data-stu-id="03e76-105">In this section, we cover the tools offered by Q# for testing and debugging quantum programs.</span></span>

## <a name="unit-tests"></a><span data-ttu-id="03e76-106">Testes de Unidade</span><span class="sxs-lookup"><span data-stu-id="03e76-106">Unit Tests</span></span>

<span data-ttu-id="03e76-107">Uma abordagem comum para testar programas clássicos é escrever pequenos programas chamados *testes unitários* que executam código em uma biblioteca e comparar sua saída com alguma saída esperada.</span><span class="sxs-lookup"><span data-stu-id="03e76-107">One common approach to testing classical programs is to write small programs called *unit tests* which run code in a library and compare its output to some expected output.</span></span>
<span data-ttu-id="03e76-108">Por exemplo, podemos querer `Square(2)` garantir `4`esse retorno, já que sabemos *a priori* que $2^2 = 4$.</span><span class="sxs-lookup"><span data-stu-id="03e76-108">For instance, we may want to ensure that `Square(2)` returns `4`, since we know *a priori* that $2^2 = 4$.</span></span>

<span data-ttu-id="03e76-109">Q# suporta a criação de testes unitários para programas quânticos, e que podem ser executados como testes dentro da estrutura de teste da unidade [xUnit.](https://xunit.github.io/)</span><span class="sxs-lookup"><span data-stu-id="03e76-109">Q# supports creating unit tests for quantum programs, and which can be executed as tests within the [xUnit](https://xunit.github.io/) unit testing framework.</span></span>

### <a name="creating-a-test-project"></a><span data-ttu-id="03e76-110">Criando um projeto de teste</span><span class="sxs-lookup"><span data-stu-id="03e76-110">Creating a Test Project</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="03e76-111">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="03e76-111">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="03e76-112">Abra o Visual Studio 2019.</span><span class="sxs-lookup"><span data-stu-id="03e76-112">Open Visual Studio 2019.</span></span> <span data-ttu-id="03e76-113">Vá para `File` o `New`  >  `Project...`menu e selecione .</span><span class="sxs-lookup"><span data-stu-id="03e76-113">Go to the `File` menu and select `New` > `Project...`.</span></span>
<span data-ttu-id="03e76-114">No canto superior direito, procure `Q#` `Q# Test Project` e selecione o modelo.</span><span class="sxs-lookup"><span data-stu-id="03e76-114">In the upper right corner, search for `Q#`, and select the `Q# Test Project` template.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="03e76-115">Linha de comando/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="03e76-115">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="03e76-116">Na sua linha de comando favorita, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="03e76-116">From your favorite command line, run the following command:</span></span>
```bash
$ dotnet new xunit -lang Q# -o Tests
$ cd Tests
$ code . # To open in Visual Studio Code
```

****

<span data-ttu-id="03e76-117">Seu novo projeto terá `Tests.qs`um único arquivo, que fornece um lugar conveniente para definir novos testes de unidade Q#.</span><span class="sxs-lookup"><span data-stu-id="03e76-117">Your new project will have a single file `Tests.qs`, which provides a convenient place to define new Q# unit tests.</span></span>
<span data-ttu-id="03e76-118">Inicialmente, este arquivo `AllocateQubit` contém um teste de unidade de amostra que{0}verifica se um qubit recém-alocado está no estado de $\ket $ e imprime uma mensagem:</span><span class="sxs-lookup"><span data-stu-id="03e76-118">Initially this file contains one sample unit test `AllocateQubit` which checks that a newly allocated qubit is in the $\ket{0}$ state and prints a message:</span></span>

```qsharp
    @Test("QuantumSimulator")
    operation AllocateQubit () : Unit {

        using (qubit = Qubit()) {
            Assert([PauliZ], [qubit], Zero, "Newly allocated qubit must be in the |0⟩ state.");
        }
        
        Message("Test passed");
    }
```

:novo: <span data-ttu-id="03e76-119">Qualquer operação Q# ou função `Unit` que `Unit` leve um argumento de tipo `@Test("...")` e retorno pode ser marcada como um teste de unidade através do atributo.</span><span class="sxs-lookup"><span data-stu-id="03e76-119">Any Q# operation or function that takes an argument of type `Unit` and returns `Unit` can be marked as a unit test via the `@Test("...")` attribute.</span></span> <span data-ttu-id="03e76-120">O argumento para `"QuantumSimulator"` esse atributo, acima, especifica o destino no qual o teste é executado.</span><span class="sxs-lookup"><span data-stu-id="03e76-120">The argument to that attribute, `"QuantumSimulator"` above, specifies the target on which the test is executed.</span></span> <span data-ttu-id="03e76-121">Um único teste pode ser executado em vários alvos.</span><span class="sxs-lookup"><span data-stu-id="03e76-121">A single test can be executed on multiple targets.</span></span> <span data-ttu-id="03e76-122">Por exemplo, adicione `@Test("ResourcesEstimator")` `AllocateQubit`um atributo acima .</span><span class="sxs-lookup"><span data-stu-id="03e76-122">For example, add an attribute `@Test("ResourcesEstimator")` above `AllocateQubit`.</span></span> 
```qsharp
    @Test("QuantumSimulator")
    @Test("ResourcesEstimator")
    operation AllocateQubit () : Unit {
        ...
```
<span data-ttu-id="03e76-123">Salve o arquivo e execute todos os testes.</span><span class="sxs-lookup"><span data-stu-id="03e76-123">Save the file and execute all tests.</span></span> <span data-ttu-id="03e76-124">Agora devem ser realizados dois testes de unidade, um em que o AllocateQubit é executado no QuantumSimulator e outro onde ele é executado no ResourceEstimator.</span><span class="sxs-lookup"><span data-stu-id="03e76-124">There should now be two unit tests, one where AllocateQubit is executed on the QuantumSimulator, and one where it is executed in the ResourceEstimator.</span></span> 

<span data-ttu-id="03e76-125">O compilador Q# reconhece os alvos incorporados "QuantumSimulator", "ToffoliSimulator" e "ResourcesEstimator" como alvos de execução válidos para testes unitários.</span><span class="sxs-lookup"><span data-stu-id="03e76-125">The Q# compiler recognizes the built-in targets "QuantumSimulator", "ToffoliSimulator", and "ResourcesEstimator" as valid execution targets for unit tests.</span></span> <span data-ttu-id="03e76-126">Também é possível especificar qualquer nome totalmente qualificado para definir um alvo de execução personalizado.</span><span class="sxs-lookup"><span data-stu-id="03e76-126">It is also possible to specify any fully qualified name to define a custom execution target.</span></span> 

### <a name="running-q-unit-tests"></a><span data-ttu-id="03e76-127">Executando testes de unidade Q#</span><span class="sxs-lookup"><span data-stu-id="03e76-127">Running Q# Unit Tests</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="03e76-128">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="03e76-128">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="03e76-129">Como uma configuração única por solução, `Test` vá `Test Settings`  >  `Default Processor Architecture`  > para o menu e selecione `X64`.</span><span class="sxs-lookup"><span data-stu-id="03e76-129">As a one-time per-solution setup, go to `Test` menu and select `Test Settings` > `Default Processor Architecture` > `X64`.</span></span>

> [!TIP]
> <span data-ttu-id="03e76-130">A configuração padrão da arquitetura do processador`.suo`para o Visual Studio é armazenada no arquivo de opções de solução () para cada solução.</span><span class="sxs-lookup"><span data-stu-id="03e76-130">The default processor architecture setting for Visual Studio is stored in the solution options (`.suo`) file for each solution.</span></span>
> <span data-ttu-id="03e76-131">Se você excluir este arquivo, então `X64` você precisará selecionar como sua arquitetura de processador novamente.</span><span class="sxs-lookup"><span data-stu-id="03e76-131">If you delete this file, then you will need to select `X64` as your processor architecture again.</span></span>

<span data-ttu-id="03e76-132">Construa o projeto, `Test` vá `Windows`  >  `Test Explorer`para o menu e selecione .</span><span class="sxs-lookup"><span data-stu-id="03e76-132">Build the project, go to the `Test` menu and select `Windows` > `Test Explorer`.</span></span> <span data-ttu-id="03e76-133">`AllocateQubit`aparecerão na lista de testes `Not Run Tests` no grupo.</span><span class="sxs-lookup"><span data-stu-id="03e76-133">`AllocateQubit` will show up in the list of tests in the `Not Run Tests` group.</span></span> <span data-ttu-id="03e76-134">Selecione `Run All` ou execute este teste individual, e ele deve passar!</span><span class="sxs-lookup"><span data-stu-id="03e76-134">Select `Run All` or run this individual test, and it should pass!</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="03e76-135">Linha de comando/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="03e76-135">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="03e76-136">Para executar os testes, navegue até `Tests.csproj`a pasta do projeto (a pasta que contém), e execute o comando:</span><span class="sxs-lookup"><span data-stu-id="03e76-136">To run tests, navigate to the project folder (the folder which contains `Tests.csproj`), and execute the command:</span></span>

```bash
$ dotnet restore
$ dotnet test
```

<span data-ttu-id="03e76-137">Você deve ver um resultado semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="03e76-137">You should get output similar to the following:</span></span>

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

<span data-ttu-id="03e76-138">Os testes unitários podem ser filtrados de acordo com seu nome e/ou o alvo de execução:</span><span class="sxs-lookup"><span data-stu-id="03e76-138">Unit tests can be filtered according to their name and/or the execution target:</span></span>

```bash 
$ dotnet test --filter "Target=QuantumSimulator"
$ dotnet test --filter "Name=AllocateQubit"
```


***

<span data-ttu-id="03e76-139">A função <xref:microsoft.quantum.intrinsic.message> intrínseca `(String -> Unit)` tem tipo e permite a criação de mensagens de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="03e76-139">The intrinsic function <xref:microsoft.quantum.intrinsic.message> has type `(String -> Unit)` and enables the creation of diagnostic messages.</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="03e76-140">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="03e76-140">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="03e76-141">Depois de executar um teste no Test Explorer e clicar no teste, um painel aparecerá com informações sobre a execução do teste: status aprovado/falhado, tempo decorrido e um link "Saída".</span><span class="sxs-lookup"><span data-stu-id="03e76-141">After you execute a test in Test Explorer and click on the test, a panel will appear with information about test execution: Passed/Failed status, elapsed time and an "Output" link.</span></span> <span data-ttu-id="03e76-142">Se você clicar no link "Saída", a saída de teste será aberta em uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="03e76-142">If you click the "Output" link, test output will open in a new window.</span></span>

![saída de teste](~/media/unit-test-output.png)

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="03e76-144">Linha de comando/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="03e76-144">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="03e76-145">O status de aprovação/falha de cada `dotnet test`teste é impresso no console por .</span><span class="sxs-lookup"><span data-stu-id="03e76-145">The pass/fail status for each test is printed to the console by `dotnet test`.</span></span>
<span data-ttu-id="03e76-146">Para testes de falha, as saídas também são impressas no console para ajudar a diagnosticar a falha.</span><span class="sxs-lookup"><span data-stu-id="03e76-146">For failing tests, the outputs are also printed to the console to help diagnose the failure.</span></span>

***

## <a name="facts-and-assertions"></a><span data-ttu-id="03e76-147">Fatos e Afirmações</span><span class="sxs-lookup"><span data-stu-id="03e76-147">Facts and Assertions</span></span>

<span data-ttu-id="03e76-148">Como as funções em Q# não têm efeitos _colaterais lógicos,_ quaisquer _outros tipos_ `()` de efeitos da execução de uma função cujo tipo de saída é a tupla vazia nunca podem ser observados dentro de um programa Q#.</span><span class="sxs-lookup"><span data-stu-id="03e76-148">Because functions in Q# have no _logical_ side effects, any _other kinds_ of effects of executing a function whose output type is the empty tuple `()` can never be observed from within a Q# program.</span></span>
<span data-ttu-id="03e76-149">Ou seja, uma máquina de destino pode `()` optar por não executar qualquer função que retorne com a garantia de que essa omissão não modificará o comportamento de qualquer código Q# seguinte.</span><span class="sxs-lookup"><span data-stu-id="03e76-149">That is, a target machine can choose not to execute any function which returns `()` with the guarantee that this omission will not modify the behavior of any following Q# code.</span></span>
<span data-ttu-id="03e76-150">Isso faz com `()` que as funções retornem (ou `Unit`seja) uma ferramenta útil para incorporar afirmações e depurar lógica em programas Q#.</span><span class="sxs-lookup"><span data-stu-id="03e76-150">This makes functions returning `()` (i.e. `Unit`) a useful tool for embedding assertions and debugging logic into Q# programs.</span></span> 

<span data-ttu-id="03e76-151">Vamos considerar um exemplo simples:</span><span class="sxs-lookup"><span data-stu-id="03e76-151">Let's consider a simple example:</span></span>

```qsharp
function PositivityFact(value : Double) : Unit 
{
    if (value <= 0) 
    {
        fail "Expected a positive number.";
    }
}
```

<span data-ttu-id="03e76-152">Aqui, a `fail` palavra-chave indica que a computação não deve prosseguir, levantando uma exceção na máquina de destino que executa o programa Q#.</span><span class="sxs-lookup"><span data-stu-id="03e76-152">Here, the keyword `fail` indicates that the computation should not proceed, raising an exception in the target machine running the Q# program.</span></span>
<span data-ttu-id="03e76-153">Por definição, uma falha desse tipo não pode ser observada dentro de Q#, pois nenhum código Q# adicional é executado após uma `fail` declaração ser alcançada.</span><span class="sxs-lookup"><span data-stu-id="03e76-153">By definition, a failure of this kind cannot be observed from within Q#, as no further Q# code is run after a `fail` statement is reached.</span></span>
<span data-ttu-id="03e76-154">Assim, se passarmos por `PositivityFact`uma chamada para , podemos ter certeza de que sua contribuição foi positiva.</span><span class="sxs-lookup"><span data-stu-id="03e76-154">Thus, if we proceed past a call to `PositivityFact`, we can be assured by that its input was positive.</span></span>

<span data-ttu-id="03e76-155">Observe que podemos implementar o `PositivityFact` mesmo [`Fact`](xref:microsoft.quantum.diagnostics.fact) comportamento <xref:microsoft.quantum.diagnostics> que usar a função a partir do namespace:</span><span class="sxs-lookup"><span data-stu-id="03e76-155">Note that we can implement the same behavior as `PositivityFact` using the [`Fact`](xref:microsoft.quantum.diagnostics.fact) function from the <xref:microsoft.quantum.diagnostics> namespace:</span></span>

```qsharp
    Fact(value > 0, "Expected a positive number.");
```

<span data-ttu-id="03e76-156">*As afirmações,* por outro lado, são usadas de forma semelhante aos fatos, mas podem depender do estado da máquina alvo.</span><span class="sxs-lookup"><span data-stu-id="03e76-156">*Assertions*, on the other hand, are used similarly to facts, but may be dependent on the state of the target machine.</span></span> <span data-ttu-id="03e76-157">Correspondentemente, são definidas como operações, enquanto os fatos são definidos como funções (como acima).</span><span class="sxs-lookup"><span data-stu-id="03e76-157">Correspondingly, they are defined as operations, whereas facts are defined as functions (as above).</span></span>
<span data-ttu-id="03e76-158">Para entender a distinção, considere o seguinte uso de um fato dentro de uma afirmação:</span><span class="sxs-lookup"><span data-stu-id="03e76-158">To understand the distinction, consider the following use of a fact within an assertion:</span></span>

```qsharp
operation AssertQubitsAreAvailable() : Unit
{
     Fact(GetQubitsAvailableToUse() > 0, "No qubits were actually available");
}
```

<span data-ttu-id="03e76-159">Aqui, estamos usando <xref:microsoft.quantum.environment.getqubitsavailabletouse> a operação para retornar o número de qubits disponíveis para uso.</span><span class="sxs-lookup"><span data-stu-id="03e76-159">Here, we are using the operation <xref:microsoft.quantum.environment.getqubitsavailabletouse> to return the number of qubits available to use.</span></span>
<span data-ttu-id="03e76-160">Como isso depende claramente do estado global do programa e `AssertQubitsAreAvailable` do seu ambiente de execução, nossa definição deve ser uma operação também.</span><span class="sxs-lookup"><span data-stu-id="03e76-160">As this clearly depends on the global state of the program and its execution environment, our definition of  `AssertQubitsAreAvailable` must be an operation as well.</span></span>
<span data-ttu-id="03e76-161">No entanto, podemos usar esse `Bool` estado global para `Fact` produzir um valor simples como entrada para a função.</span><span class="sxs-lookup"><span data-stu-id="03e76-161">However, we can use that global state to yield a simple `Bool` value as input to the `Fact` function.</span></span>

<span data-ttu-id="03e76-162">Com base nessas ideias, [o prelúdio](xref:microsoft.quantum.libraries.standard.prelude) <xref:microsoft.quantum.intrinsic.assert> oferece <xref:microsoft.quantum.intrinsic.assertprob> duas afirmações especialmente `()`úteis, e ambas modeladas como operações para .</span><span class="sxs-lookup"><span data-stu-id="03e76-162">Building on these ideas, [the prelude](xref:microsoft.quantum.libraries.standard.prelude) offers two especially useful assertions, <xref:microsoft.quantum.intrinsic.assert> and <xref:microsoft.quantum.intrinsic.assertprob> both modeled as operations onto `()`.</span></span> <span data-ttu-id="03e76-163">Essas afirmações tomam cada um um operador de Pauli descrevendo uma medição particular de interesse, um registro quântico no qual uma medição deve ser realizada, e um resultado hipotético.</span><span class="sxs-lookup"><span data-stu-id="03e76-163">These assertions each take a Pauli operator describing a particular measurement of interest, a quantum register on which a measurement is to be performed, and a hypothetical outcome.</span></span>
<span data-ttu-id="03e76-164">Em máquinas-alvo que funcionam por simulação, não estamos vinculados [ao teorema da não clonagem,](https://en.wikipedia.org/wiki/No-cloning_theorem)e podemos realizar tais medições sem perturbar o registro passado a tais afirmações.</span><span class="sxs-lookup"><span data-stu-id="03e76-164">On target machines which work by simulation, we are not bound by [the no-cloning theorem](https://en.wikipedia.org/wiki/No-cloning_theorem), and can perform such measurements without disturbing the register passed to such assertions.</span></span>
<span data-ttu-id="03e76-165">Um simulador pode, então, semelhante à função acima, abortar a `PositivityFact` computação se o resultado hipotético não for observado na prática:</span><span class="sxs-lookup"><span data-stu-id="03e76-165">A simulator can then, similar to the `PositivityFact` function above, abort computation if the hypothetical outcome would not be observed in practice:</span></span>

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

<span data-ttu-id="03e76-166">No hardware quântico físico, onde o teorema sem clonagem `Assert` `AssertProb` impede o `()` exame do estado quântico, as operações simplesmente retornam sem outro efeito.</span><span class="sxs-lookup"><span data-stu-id="03e76-166">On physical quantum hardware, where the no-cloning theorem prevents examination of quantum state, the `Assert` and `AssertProb` operations simply return `()` with no other effect.</span></span>

<span data-ttu-id="03e76-167">O <xref:microsoft.quantum.diagnostics> namespace fornece várias `Assert` outras funções da família que nos permitem verificar condições mais avançadas.</span><span class="sxs-lookup"><span data-stu-id="03e76-167">The <xref:microsoft.quantum.diagnostics> namespace provides several more functions of the `Assert` family which allow us to check more advanced conditions.</span></span> 

## <a name="dump-functions"></a><span data-ttu-id="03e76-168">Funções de despejo</span><span class="sxs-lookup"><span data-stu-id="03e76-168">Dump Functions</span></span>

<span data-ttu-id="03e76-169">Para ajudar a solucionar problemas de programas quânticos, o <xref:microsoft.quantum.diagnostics> namespace <xref:microsoft.quantum.diagnostics.dumpmachine> oferece <xref:microsoft.quantum.diagnostics.dumpregister>duas funções que podem despejar em um arquivo o status atual da máquina de destino: e .</span><span class="sxs-lookup"><span data-stu-id="03e76-169">To help troubleshooting quantum programs, the <xref:microsoft.quantum.diagnostics> namespace offers two functions that can dump into a file the current status of the target machine: <xref:microsoft.quantum.diagnostics.dumpmachine> and <xref:microsoft.quantum.diagnostics.dumpregister>.</span></span> <span data-ttu-id="03e76-170">A saída gerada de cada um depende da máquina alvo.</span><span class="sxs-lookup"><span data-stu-id="03e76-170">The generated output of each depends on the target machine.</span></span>

### <a name="dumpmachine"></a><span data-ttu-id="03e76-171">DumpMachine</span><span class="sxs-lookup"><span data-stu-id="03e76-171">DumpMachine</span></span>

<span data-ttu-id="03e76-172">O simulador quântico de estado completo distribuído como parte do Kit de Desenvolvimento Quântico escreve no arquivo a função de [onda](https://en.wikipedia.org/wiki/Wave_function) de todo o sistema quântico, como uma matriz unidimensional de números complexos, em que cada elemento representa a amplitude da probabilidade de medir o estado de base computacional $\ket{n}$, onde $\ket{n} = \ket{b_{n-1}... b_1b_0}$ por bits $\{b_i\}$.</span><span class="sxs-lookup"><span data-stu-id="03e76-172">The full-state quantum simulator distributed as part of the Quantum Development Kit writes into the file the [wave function](https://en.wikipedia.org/wiki/Wave_function) of the entire quantum system, as a one-dimensional array of complex numbers, in which each element represents the amplitude of the probability of measuring the computational basis state $\ket{n}$, where $\ket{n} = \ket{b_{n-1}...b_1b_0}$ for bits $\{b_i\}$.</span></span> <span data-ttu-id="03e76-173">Por exemplo, em uma máquina com apenas dois qubits alocados e no estado quântico $${1}\start{align} \ket{\psi} = \frac {\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10}, \end{align} $$ a chamada <xref:microsoft.quantum.diagnostics.dumpmachine> gera essa saída:</span><span class="sxs-lookup"><span data-stu-id="03e76-173">For example, on a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10}, \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpmachine> generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0;1
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣2❭:    -0.500000 + -0.500000 i  ==     **********           [ 0.500000 ]   /     [ -2.35619 rad ]
∣3❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="03e76-174">A primeira linha fornece um comentário com os IDs dos qubits correspondentes em sua ordem significativa.</span><span class="sxs-lookup"><span data-stu-id="03e76-174">The first row provides a comment with the IDs of the corresponding qubits in their significant order.</span></span>
<span data-ttu-id="03e76-175">O resto das linhas descrevem a amplitude de probabilidade de medir o vetor de estado base $\ket{n}$ em formatos cartesiano e polar.</span><span class="sxs-lookup"><span data-stu-id="03e76-175">The rest of the rows describe the probability amplitude of measuring the basis state vector $\ket{n}$ in both Cartesian and polar formats.</span></span> <span data-ttu-id="03e76-176">Em detalhes para a primeira linha:</span><span class="sxs-lookup"><span data-stu-id="03e76-176">In detail for the first row:</span></span>

* <span data-ttu-id="03e76-177">**`∣0❭:`** esta linha corresponde `0` ao estado de base computacional</span><span class="sxs-lookup"><span data-stu-id="03e76-177">**`∣0❭:`** this row corresponds to the `0` computational basis state</span></span>
* <span data-ttu-id="03e76-178">**`0.707107 +  0.000000 i`**: a amplitude de probabilidade no formato cartesiano.</span><span class="sxs-lookup"><span data-stu-id="03e76-178">**`0.707107 +  0.000000 i`**: the probability amplitude in Cartesian format.</span></span>
* <span data-ttu-id="03e76-179">**` == `**: `equal` o sinal separa ambas as representações equivalentes.</span><span class="sxs-lookup"><span data-stu-id="03e76-179">**` == `**: the `equal` sign seperates both equivalent representations.</span></span>
* <span data-ttu-id="03e76-180">**`**********  `**: Uma representação gráfica da magnitude, o número de `*` é proporcional à probabilidade de medir este vetor de estado.</span><span class="sxs-lookup"><span data-stu-id="03e76-180">**`**********  `**: A graphical representation of the magnitude, the number of `*` is proportionate to the probability of measuring this state vector.</span></span>
* <span data-ttu-id="03e76-181">**`[ 0.500000 ]`**: o valor numérico da magnitude</span><span class="sxs-lookup"><span data-stu-id="03e76-181">**`[ 0.500000 ]`**: the numeric value of the magnitude</span></span>
* <span data-ttu-id="03e76-182">**`    ---`**: Representação gráfica da fase da amplitude (veja abaixo).</span><span class="sxs-lookup"><span data-stu-id="03e76-182">**`    ---`**: A graphical representation of the amplitude's phase (see below).</span></span>
* <span data-ttu-id="03e76-183">**`[ 0.0000 rad ]`**: o valor numérico da fase (em radianos).</span><span class="sxs-lookup"><span data-stu-id="03e76-183">**`[ 0.0000 rad ]`**: the numeric value of the phase (in radians).</span></span>

<span data-ttu-id="03e76-184">Tanto a magnitude quanto a fase são exibidas com uma representação gráfica.</span><span class="sxs-lookup"><span data-stu-id="03e76-184">Both the magnitude and the phase are displayed with a graphical representation.</span></span> <span data-ttu-id="03e76-185">A representação de magnitude é direta: `*`mostra uma barra de , quanto maior a probabilidade, maior será a barra.</span><span class="sxs-lookup"><span data-stu-id="03e76-185">The magnitude representation is straight-forward: it shows a bar of `*`, the bigger the probability the bigger the bar will be.</span></span> <span data-ttu-id="03e76-186">Para a fase, mostramos os seguintes símbolos para representar o ângulo com base em intervalos:</span><span class="sxs-lookup"><span data-stu-id="03e76-186">For the phase, we show the following symbols to represent the angle based on ranges:</span></span>

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

<span data-ttu-id="03e76-187">Os exemplos a `DumpMachine` seguir mostram para alguns estados comuns:</span><span class="sxs-lookup"><span data-stu-id="03e76-187">The following examples show `DumpMachine` for some common states:</span></span>

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
  > <span data-ttu-id="03e76-188">O id de um qubit é atribuído em tempo de execução e não está necessariamente alinhado com a ordem em que o qubit foi alocado ou sua posição dentro de um registro de qubit.</span><span class="sxs-lookup"><span data-stu-id="03e76-188">The id of a qubit is assigned at runtime and it's not necessarily aligned with the order in which the qubit was allocated or its position within a qubit register.</span></span>


#### <a name="visual-studio-2019"></a>[<span data-ttu-id="03e76-189">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="03e76-189">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

  > [!TIP]
  > <span data-ttu-id="03e76-190">Você pode descobrir um id de qubit no Visual Studio colocando um ponto de ruptura em seu código e inspecionando o valor de uma variável de qubit, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="03e76-190">You can figure out a qubit id in Visual Studio by putting a breakpoint in your code and inspecting the value of a qubit variable, for example:</span></span>
  > 
  > ![mostrar id qubit no Visual Studio](~/media/qubit_id.png)
  >
  > <span data-ttu-id="03e76-192">o qubit `0` com `register2` índice em`3`has id= `1` , o`2`qubit com índice tem id= .</span><span class="sxs-lookup"><span data-stu-id="03e76-192">the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="03e76-193">Linha de comando/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="03e76-193">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

  > [!TIP]
  > <span data-ttu-id="03e76-194">Você pode descobrir um id de <xref:microsoft.quantum.intrinsic.message> qubit usando a função e passando a variável qubit na mensagem, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="03e76-194">You can figure out a qubit id by using the <xref:microsoft.quantum.intrinsic.message> function and passing the qubit variable in the message, for example:</span></span>
  >
  > ```qsharp
  > Message($"0={register2[0]}; 1={register2[1]}");
  > ```
  > 
  > <span data-ttu-id="03e76-195">que poderia gerar essa saída:</span><span class="sxs-lookup"><span data-stu-id="03e76-195">which could generate this output:</span></span>
  >```
  > 0=q:3; 1=q:2
  >```
  > <span data-ttu-id="03e76-196">o que significa que `0` o `register2` qubit`3`com índice ligado `1` tem id= , o qubit com índice tem id=`2`.</span><span class="sxs-lookup"><span data-stu-id="03e76-196">which means that the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>


***

<span data-ttu-id="03e76-197"><xref:microsoft.quantum.diagnostics.dumpmachine>faz parte <xref:microsoft.quantum.diagnostics> do namespace, então para usá-lo `open` você deve adicionar uma declaração:</span><span class="sxs-lookup"><span data-stu-id="03e76-197"><xref:microsoft.quantum.diagnostics.dumpmachine> is part of the  <xref:microsoft.quantum.diagnostics> namespace, so in order to use it you must add an `open` statement:</span></span>

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


### <a name="dumpregister"></a><span data-ttu-id="03e76-198">DumpRegister</span><span class="sxs-lookup"><span data-stu-id="03e76-198">DumpRegister</span></span>

<span data-ttu-id="03e76-199"><xref:microsoft.quantum.diagnostics.dumpregister>funciona <xref:microsoft.quantum.diagnostics.dumpmachine>como , exceto que também é preciso um conjunto de qubits para limitar a quantidade de informações apenas a que é relevante para os qubits correspondentes.</span><span class="sxs-lookup"><span data-stu-id="03e76-199"><xref:microsoft.quantum.diagnostics.dumpregister> works like <xref:microsoft.quantum.diagnostics.dumpmachine>, except it also takes an array of qubits to limit the amount of information to only that relevant to the corresponding qubits.</span></span>

<span data-ttu-id="03e76-200">Como <xref:microsoft.quantum.diagnostics.dumpmachine>acontece, as <xref:microsoft.quantum.diagnostics.dumpregister> informações geradas pela máquina alvo dependem da máquina alvo.</span><span class="sxs-lookup"><span data-stu-id="03e76-200">As with <xref:microsoft.quantum.diagnostics.dumpmachine>, the information generated by <xref:microsoft.quantum.diagnostics.dumpregister> depends on the target machine.</span></span> <span data-ttu-id="03e76-201">Para o simulador quântico de estado completo, ele grava no arquivo a função de onda até uma fase global <xref:microsoft.quantum.diagnostics.dumpmachine>do subsistema quântico gerado pelos qubits fornecidos no mesmo formato que .</span><span class="sxs-lookup"><span data-stu-id="03e76-201">For the full-state quantum simulator it writes into the file the wave function up to a global phase of the quantum sub-system generated by the provided qubits in the same format as <xref:microsoft.quantum.diagnostics.dumpmachine>.</span></span>  <span data-ttu-id="03e76-202">Por{1}exemplo, pegue novamente uma máquina com apenas dois qubits alocados e no estado quântico $$ \start{align}{2}\ket{\psi} = \frac {\sqrt } \ket{00} - \frac{(1 + i)}{2} \ket{10} = - e^{-i\pi/4 } ({1}(\frac {\sqrt{2}} \ket{0} - \frac{(1 + i)}{2} \ket{1} ) \otimes \frac{-(1 + i)}{\sqrt{2}} \ket{0} ) , \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[0]` generates this output:</span><span class="sxs-lookup"><span data-stu-id="03e76-202">For example, take again a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10} = - e^{-i\pi/4} ( (\frac{1}{\sqrt{2}} \ket{0} - \frac{(1 + i)}{2} \ket{1} ) \otimes \frac{-(1 + i)}{\sqrt{2}} \ket{0} ) , \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[0]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:    -0.707107 + -0.707107 i  ==     ******************** [ 1.000000 ]  /      [ -2.35619 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="03e76-203">e <xref:microsoft.quantum.diagnostics.dumpregister> chamar `qubit[1]` para gera essa saída:</span><span class="sxs-lookup"><span data-stu-id="03e76-203">and calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[1]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 1
∣0❭:     0.707107 +  0.000000 i  ==     ***********          [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:    -0.500000 + -0.500000 i  ==     ***********          [ 0.500000 ]  /      [ -2.35619 rad ]
```

<span data-ttu-id="03e76-204">Em geral, o estado de um registro que está emaranhado com outro registro é um estado misto e não um estado puro.</span><span class="sxs-lookup"><span data-stu-id="03e76-204">In general, the state of a register that is entangled with another register is a mixed state rather than a pure state.</span></span> <span data-ttu-id="03e76-205">Neste caso, <xref:microsoft.quantum.diagnostics.dumpregister> produz a seguinte mensagem:</span><span class="sxs-lookup"><span data-stu-id="03e76-205">In this case, <xref:microsoft.quantum.diagnostics.dumpregister> outputs the following message:</span></span>

```
Qubits provided (0;) are entangled with some other qubit.
```

<span data-ttu-id="03e76-206">O exemplo a seguir mostra <xref:microsoft.quantum.diagnostics.dumpregister> como <xref:microsoft.quantum.diagnostics.dumpmachine> você pode usar ambos e em seu código Q#:</span><span class="sxs-lookup"><span data-stu-id="03e76-206">The following example shows you how you can use both <xref:microsoft.quantum.diagnostics.dumpregister> and <xref:microsoft.quantum.diagnostics.dumpmachine> in your Q# code:</span></span>

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

## <a name="debugging"></a><span data-ttu-id="03e76-207">Depuração</span><span class="sxs-lookup"><span data-stu-id="03e76-207">Debugging</span></span>

<span data-ttu-id="03e76-208">Além das `Assert` `Dump` funções e operações, q# suporta um subconjunto de recursos padrão de depuração visual Studio: definir pontos de interrupção de [linha,](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints) [passar pelo código usando F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) e [inspecionar valores de variáveis clássicas](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) são todos possíveis durante a execução de código no simulador.</span><span class="sxs-lookup"><span data-stu-id="03e76-208">On top of `Assert` and `Dump` functions and operations, Q# supports a subset of standard Visual Studio debugging capabilities: [setting line breakpoints](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), [stepping through code using F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) and [inspecting values of classic variables](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) are all possible during code execution on the simulator.</span></span>

<span data-ttu-id="03e76-209">A depuração no Visual Studio Code aproveita os recursos de depuração fornecidos pela extensão C# for Visual Studio Code alimentada pelo OmniSharp e requer a instalação da [versão mais recente](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp).</span><span class="sxs-lookup"><span data-stu-id="03e76-209">Debugging in Visual Studio Code leverages the debugging capabilities provided by the C# for Visual Studio Code extension powered by OmniSharp and requires installing the [latest version](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp).</span></span> 
