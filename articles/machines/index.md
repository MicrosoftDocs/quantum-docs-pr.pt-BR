---
title: Simuladores e aplicativos host quânticos | Microsoft Docs
description: Descreve como impulsionar simuladores de quantum com uma linguagem .NET de computação clássica, normalmente, C# ou Q#.
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines
ms.openlocfilehash: 14aed75ed0ed192f88699b1c7dbacfae23f74642
ms.sourcegitcommit: 9d1c045cf1a2c3e19030cb38dbc7496dbd24ab58
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2020
ms.locfileid: "73442219"
---
# <a name="quantum-simulators-and-host-applications"></a><span data-ttu-id="d7236-103">Simuladores e aplicativos host quânticos</span><span class="sxs-lookup"><span data-stu-id="d7236-103">Quantum simulators and host applications</span></span>

## <a name="what-youll-learn"></a><span data-ttu-id="d7236-104">O que você vai aprender</span><span class="sxs-lookup"><span data-stu-id="d7236-104">What You'll Learn</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="d7236-105">Como os algoritmos quânticos são executados</span><span class="sxs-lookup"><span data-stu-id="d7236-105">How quantum algorithms are executed</span></span>
> * <span data-ttu-id="d7236-106">Quais simuladores de quantum estão incluídos nesta versão</span><span class="sxs-lookup"><span data-stu-id="d7236-106">What quantum simulators are included in this release</span></span>
> * <span data-ttu-id="d7236-107">Como escrever um driver C# para o algoritmo quântico</span><span class="sxs-lookup"><span data-stu-id="d7236-107">How to write a C# driver for your quantum algorithm</span></span>

## <a name="the-quantum-development-kit-execution-model"></a><span data-ttu-id="d7236-108">O modelo de execução do Quantum development kit</span><span class="sxs-lookup"><span data-stu-id="d7236-108">The Quantum Development Kit Execution Model</span></span>

<span data-ttu-id="d7236-109">Em [Como escrever um programa quântico](xref:microsoft.quantum.write-program), executamos nosso algoritmo quântico passando um objeto `QuantumSimulator` para o método `Run` da classe do algoritmo.</span><span class="sxs-lookup"><span data-stu-id="d7236-109">In [Writing a quantum program](xref:microsoft.quantum.write-program), we executed our quantum algorithm by passing a `QuantumSimulator` object to the algorithm class's `Run` method.</span></span>
<span data-ttu-id="d7236-110">A classe `QuantumSimulator` executa o algoritmo quântico simulando totalmente o vetor de estado quântico, que é perfeito para executar e testar `Teleport`.</span><span class="sxs-lookup"><span data-stu-id="d7236-110">The `QuantumSimulator` class executes the quantum algorithm by fully simulating the quantum state vector, which is perfect for running and testing `Teleport`.</span></span>
<span data-ttu-id="d7236-111">Confira o [Guia de conceitos](xref:microsoft.quantum.concepts.intro) para saber mais sobre os vetores de estado quântico.</span><span class="sxs-lookup"><span data-stu-id="d7236-111">See the [Concepts guide](xref:microsoft.quantum.concepts.intro) for more on quantum state vectors.</span></span>

<span data-ttu-id="d7236-112">Outros computadores de destino podem ser usados para executar um algoritmo quântico.</span><span class="sxs-lookup"><span data-stu-id="d7236-112">Other target machines may be used to run a quantum algorithm.</span></span>
<span data-ttu-id="d7236-113">O computador é responsável por fornecer implementações de primitivos quânticos para o algoritmo.</span><span class="sxs-lookup"><span data-stu-id="d7236-113">The machine is responsible for providing implementations of quantum primitives for the algorithm.</span></span>
<span data-ttu-id="d7236-114">Isso inclui operações primitivas, como H, CNOT e Measure, bem como gerenciamento e acompanhamento de qubits.</span><span class="sxs-lookup"><span data-stu-id="d7236-114">This includes primitive operations such as H, CNOT, and Measure, as well as qubit management and tracking.</span></span>
<span data-ttu-id="d7236-115">Diferentes classes de computadores quânticos representam modelos de execução diferentes para o mesmo algoritmo quântico.</span><span class="sxs-lookup"><span data-stu-id="d7236-115">Different classes of quantum machines represent different execution models for the same quantum algorithm.</span></span>

<span data-ttu-id="d7236-116">Cada tipo de computador quântico pode fornecer diferentes implementações desses primitivos.</span><span class="sxs-lookup"><span data-stu-id="d7236-116">Each type of quantum machine may provide different implementations of these primitives.</span></span>
<span data-ttu-id="d7236-117">Por exemplo, o simulador de rastreamento do computador quântico incluído no kit de desenvolvimento não faz nenhuma simulação.</span><span class="sxs-lookup"><span data-stu-id="d7236-117">For instance, the quantum computer trace simulator included in the development kit doesn't do any simulation at all.</span></span>
<span data-ttu-id="d7236-118">Em vez disso, ele rastreia o uso de portões, qubits e outros recursos para o algoritmo.</span><span class="sxs-lookup"><span data-stu-id="d7236-118">Rather, it tracks gate, qubit, and other resource usage for the algorithm.</span></span>

### <a name="quantum-machines"></a><span data-ttu-id="d7236-119">Computadores quânticos</span><span class="sxs-lookup"><span data-stu-id="d7236-119">Quantum Machines</span></span>

<span data-ttu-id="d7236-120">No futuro, definiremos classes adicionais de computadores quânticos para dar suporte a outros tipos de simulação e à execução em computadores quânticos topológicos.</span><span class="sxs-lookup"><span data-stu-id="d7236-120">In the future, we will define additional quantum machine classes to support other types of simulation and to support execution on topological quantum computers.</span></span>
<span data-ttu-id="d7236-121">Permitir que o algoritmo permaneça constante enquanto varia a implementação de computador subjacente facilita o teste e a depuração de um algoritmo em simulação e, em seguida, executa-o em um hardware real com a confiança de que o algoritmo não foi alterado.</span><span class="sxs-lookup"><span data-stu-id="d7236-121">Allowing the algorithm to stay constant while varying the underlying machine implementation makes it easy to test and debug an algorithm in simulation and then run it on real hardware with confidence that the algorithm hasn't changed.</span></span>

### <a name="whats-included-in-this-release"></a><span data-ttu-id="d7236-122">O que está incluído nesta versão</span><span class="sxs-lookup"><span data-stu-id="d7236-122">What's Included in this Release</span></span>

<span data-ttu-id="d7236-123">Esta versão do Kit do Desenvolvedor do Quantum inclui várias classes de computadores quânticos.</span><span class="sxs-lookup"><span data-stu-id="d7236-123">This release of the quantum developer kit includes several quantum machine classes.</span></span>
<span data-ttu-id="d7236-124">Todas elas são definidas no namespace `Microsoft.Quantum.Simulation.Simulators`.</span><span class="sxs-lookup"><span data-stu-id="d7236-124">All of them are defined in the `Microsoft.Quantum.Simulation.Simulators` namespace.</span></span>

* <span data-ttu-id="d7236-125">Um [simulador de vetor de estado completo](xref:microsoft.quantum.machines.full-state-simulator), a classe `QuantumSimulator`.</span><span class="sxs-lookup"><span data-stu-id="d7236-125">A [full state vector simulator](xref:microsoft.quantum.machines.full-state-simulator), the `QuantumSimulator` class.</span></span>
* <span data-ttu-id="d7236-126">Um [estimador de recursos simples](xref:microsoft.quantum.machines.resources-estimator), a classe `ResourcesEstimator`, permite uma análise de nível superior dos recursos necessários para executar um algoritmo quântico.</span><span class="sxs-lookup"><span data-stu-id="d7236-126">A [simple resources estimator](xref:microsoft.quantum.machines.resources-estimator), the `ResourcesEstimator` class, it allows a top level analysis of the resources needed to run a quantum algorithm.</span></span>
* <span data-ttu-id="d7236-127">Um [estimador de recursos baseado em rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro), a classe `QCTraceSimulator`, permite a análise avançada de consumos de recursos para o grafo de chamadas inteiro do algoritmo.</span><span class="sxs-lookup"><span data-stu-id="d7236-127">A [trace-based resource estimator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), the `QCTraceSimulator` class, it allows advanced analysis of resources consumptions for the algorithm's entire call-graph.</span></span>
* <span data-ttu-id="d7236-128">Um [simulador Toffoli](xref:microsoft.quantum.machines.toffoli-simulator), a classe `ToffoliSimulator`.</span><span class="sxs-lookup"><span data-stu-id="d7236-128">A [Toffoli simulator](xref:microsoft.quantum.machines.toffoli-simulator), the `ToffoliSimulator` class.</span></span>

## <a name="writing-a-host-application"></a><span data-ttu-id="d7236-129">Como escrever um aplicativo host</span><span class="sxs-lookup"><span data-stu-id="d7236-129">Writing a host application</span></span>

<span data-ttu-id="d7236-130">Em [Como escrever um programa quântico](xref:microsoft.quantum.write-program), escrevemos um driver C# simples para nosso algoritmo de teletransporte.</span><span class="sxs-lookup"><span data-stu-id="d7236-130">In [Writing a quantum program](xref:microsoft.quantum.write-program), we wrote a simple C# driver for our teleport algorithm.</span></span> <span data-ttu-id="d7236-131">Um driver C# tem quatro objetivos principais:</span><span class="sxs-lookup"><span data-stu-id="d7236-131">A C# driver has 4 main purposes:</span></span>

* <span data-ttu-id="d7236-132">Construir o computador de destino</span><span class="sxs-lookup"><span data-stu-id="d7236-132">Constructing the target machine</span></span>
* <span data-ttu-id="d7236-133">Calcular os argumentos necessários para o algoritmo quântico</span><span class="sxs-lookup"><span data-stu-id="d7236-133">Computing any arguments required for the quantum algorithm</span></span>
* <span data-ttu-id="d7236-134">Executar o algoritmo quântico usando o simulador</span><span class="sxs-lookup"><span data-stu-id="d7236-134">Running the quantum algorithm using the simulator</span></span>
* <span data-ttu-id="d7236-135">Processar o resultado da operação</span><span class="sxs-lookup"><span data-stu-id="d7236-135">Processing the result of the operation</span></span>

<span data-ttu-id="d7236-136">Aqui, discutiremos cada etapa mais detalhadamente.</span><span class="sxs-lookup"><span data-stu-id="d7236-136">Here we'll discuss each step in more detail.</span></span>

### <a name="constructing-the-target-machine"></a><span data-ttu-id="d7236-137">Construir o computador de destino</span><span class="sxs-lookup"><span data-stu-id="d7236-137">Constructing the Target Machine</span></span>

<span data-ttu-id="d7236-138">Os computadores quânticos são instâncias de classes .NET normais e, portanto, são criadas invocando o construtor delas, assim como qualquer classe .NET.</span><span class="sxs-lookup"><span data-stu-id="d7236-138">Quantum machines are instances of normal .NET classes, so they are created by invoking their constructor, just like any .NET class.</span></span>
<span data-ttu-id="d7236-139">Alguns simuladores, incluindo o `QuantumSimulator`, implementam a interface <xref:System.IDisposable?displayProperty=nameWithType> .NET e, portanto, devem ser encapsulados em uma instrução `using` C#.</span><span class="sxs-lookup"><span data-stu-id="d7236-139">Some simulators, including the `QuantumSimulator`, implement the .NET <xref:System.IDisposable?displayProperty=nameWithType> interface, and so should be wrapped in a C# `using` statement.</span></span>

### <a name="computing-arguments-for-the-algorithm"></a><span data-ttu-id="d7236-140">Como calcular argumentos para o algoritmo</span><span class="sxs-lookup"><span data-stu-id="d7236-140">Computing Arguments for the Algorithm</span></span>

<span data-ttu-id="d7236-141">Em nosso exemplo de `Teleport`, calculamos alguns argumentos relativamente artificiais para passarmos ao nosso algoritmo quântico.</span><span class="sxs-lookup"><span data-stu-id="d7236-141">In our `Teleport` example, we computed some relatively artificial arguments to pass to our quantum algorithm.</span></span>
<span data-ttu-id="d7236-142">No entanto, de modo mais geral, há dados significativos exigidos pelo algoritmo quântico e é mais fácil fornecê-los por meio do driver clássico.</span><span class="sxs-lookup"><span data-stu-id="d7236-142">More typically, however, there is significant data required by the quantum algorithm, and it is easiest to provide it from the classical driver.</span></span>

<span data-ttu-id="d7236-143">Por exemplo, ao fazer simulações químicas, o algoritmo quântico exige uma tabela grande de integrais de interação orbital molecular.</span><span class="sxs-lookup"><span data-stu-id="d7236-143">For instance, when doing chemical simulations, the quantum algorithm requires a large table of molecular orbital interaction integrals.</span></span>
<span data-ttu-id="d7236-144">Geralmente, eles são lidos de um arquivo que é fornecido durante a execução do algoritmo.</span><span class="sxs-lookup"><span data-stu-id="d7236-144">Generally these are read in from a file that is provided when running the algorithm.</span></span>
<span data-ttu-id="d7236-145">Como o Q# não tem um mecanismo para acessar o sistema de arquivos, esse tipo de dados é melhor coletado pelo driver clássico e, em seguida, passado para o método `Run` do algoritmo quântico.</span><span class="sxs-lookup"><span data-stu-id="d7236-145">Since Q# does not have a mechanism for accessing the file system, this sort of data is best collected by the classical driver and then passed to the quantum algorithm's `Run` method.</span></span>

<span data-ttu-id="d7236-146">Outro caso em que o driver clássico desempenha um papel fundamental é em métodos de variação.</span><span class="sxs-lookup"><span data-stu-id="d7236-146">Another case where the classical driver plays a key role is in variational methods.</span></span>
<span data-ttu-id="d7236-147">Nessa classe de algoritmos, um estado quântico é preparado com base em alguns parâmetros clássicos e esse estado é usado para calcular algum valor de interesse.</span><span class="sxs-lookup"><span data-stu-id="d7236-147">In this class of algorithms, a quantum state is prepared based on some classical parameters, and that state is used to compute some value of interest.</span></span>
<span data-ttu-id="d7236-148">Os parâmetros são ajustados com base em um tipo de algoritmo de aprendizado de máquina ou de escalada e o algoritmo quântico é executado novamente.</span><span class="sxs-lookup"><span data-stu-id="d7236-148">The parameters are adjusted based on some type of hill climbing or machine learning algorithm and the quantum algorithm run again.</span></span>
<span data-ttu-id="d7236-149">Para esses algoritmos, o próprio algoritmo de escalada é mais bem implementado como uma função puramente clássica que é chamada pelo driver clássico; os resultados da escalada são então passados para a próxima execução do algoritmo quântico.</span><span class="sxs-lookup"><span data-stu-id="d7236-149">For such algorithms, the hill climbing algorithm itself is best implemented as a purely classical function that is called by the classical driver; the results of the hill climbing are then passed to the next execution of the quantum algorithm.</span></span>

### <a name="running-the-quantum-algorithm"></a><span data-ttu-id="d7236-150">Como executar o algoritmo quântico</span><span class="sxs-lookup"><span data-stu-id="d7236-150">Running the Quantum Algorithm</span></span>

<span data-ttu-id="d7236-151">Essa parte é geralmente muito simples.</span><span class="sxs-lookup"><span data-stu-id="d7236-151">This part is generally very straightforward.</span></span>
<span data-ttu-id="d7236-152">Cada operação Q# é compilada em uma classe que fornece um método `Run` estático.</span><span class="sxs-lookup"><span data-stu-id="d7236-152">Each Q# operation is compiled into a class that provides a static `Run` method.</span></span>
<span data-ttu-id="d7236-153">Os argumentos para esse método são fornecidos pela tupla de argumento combinada da própria operação, mais um primeiro argumento adicional que é o simulador a ser usado na execução.</span><span class="sxs-lookup"><span data-stu-id="d7236-153">The arguments to this method are given by the flattened argument tuple of the operation itself, plus an additional first argument which is the simulator to execute with.</span></span> <span data-ttu-id="d7236-154">Para uma operação que espera a tupla nomeada do tipo `(a: String, (b: Double, c: Double))`, a contraparte combinada dela é do tipo `(String a, Double b, Double c)`.</span><span class="sxs-lookup"><span data-stu-id="d7236-154">For an operation that expects the named tuple of type `(a: String, (b: Double, c: Double))` its flattened counterpart is of type `(String a, Double b, Double c)`.</span></span>


<span data-ttu-id="d7236-155">Há algumas sutilezas ao passar argumentos para um método `Run`:</span><span class="sxs-lookup"><span data-stu-id="d7236-155">There are some subtleties when passing arguments to a `Run` method:</span></span>

* <span data-ttu-id="d7236-156">As matrizes precisam ser encapsuladas em um objeto `Microsoft.Quantum.Simulation.Core.QArray<T>`.</span><span class="sxs-lookup"><span data-stu-id="d7236-156">Arrays must be wrapped in a `Microsoft.Quantum.Simulation.Core.QArray<T>` object.</span></span>
    <span data-ttu-id="d7236-157">Uma classe `QArray` tem um construtor que pode usar qualquer coleção ordenada (`IEnumerable<T>`) de objetos apropriados.</span><span class="sxs-lookup"><span data-stu-id="d7236-157">A `QArray` class has a constructor that can take any ordered collection (`IEnumerable<T>`) of appropriate objects.</span></span>
* <span data-ttu-id="d7236-158">A tupla vazia, `()` em Q#, é representada por `QVoid.Instance` em C#.</span><span class="sxs-lookup"><span data-stu-id="d7236-158">The empty tuple, `()` in Q#, is represented by `QVoid.Instance` in C#.</span></span>
* <span data-ttu-id="d7236-159">As tuplas não vazias são representadas como instâncias `ValueTuple` do .NET.</span><span class="sxs-lookup"><span data-stu-id="d7236-159">Non-empty tuples are represented as .NET `ValueTuple` instances.</span></span>
* <span data-ttu-id="d7236-160">Os tipos definidos pelo usuário Q# são passados como o tipo base.</span><span class="sxs-lookup"><span data-stu-id="d7236-160">Q# user-defined types are passed as their base type.</span></span>
* <span data-ttu-id="d7236-161">Para passar uma operação ou uma função para um método `Run`, você precisa obter uma instância da classe da operação ou da função, usando o método `Get<>` do simulador.</span><span class="sxs-lookup"><span data-stu-id="d7236-161">To pass an operation or a function to a `Run` method, you have to obtain an   instance of the operation's or function's class, using the simulator's `Get<>` method.</span></span>

### <a name="processing-the-results"></a><span data-ttu-id="d7236-162">Como processar os resultados</span><span class="sxs-lookup"><span data-stu-id="d7236-162">Processing the Results</span></span>

<span data-ttu-id="d7236-163">Os resultados do algoritmo quântico são retornados do método `Run`.</span><span class="sxs-lookup"><span data-stu-id="d7236-163">The results of the quantum algorithm are returned from the `Run` method.</span></span>
<span data-ttu-id="d7236-164">O método `Run` é executado de maneira assíncrona e, portanto, retorna uma instância de <xref:System.Threading.Tasks.Task`1>.</span><span class="sxs-lookup"><span data-stu-id="d7236-164">The `Run` method executes asynchronously thus it returns an instance of <xref:System.Threading.Tasks.Task`1>.</span></span>
<span data-ttu-id="d7236-165">Há várias maneiras de obter os resultados da operação real.</span><span class="sxs-lookup"><span data-stu-id="d7236-165">There are multiple ways to get the actual operation's results.</span></span> <span data-ttu-id="d7236-166">A mais simples é usar a [propriedade `Result`](https://docs.microsoft.com/dotnet/api/system.threading.tasks.task-1.result) de `Task`:</span><span class="sxs-lookup"><span data-stu-id="d7236-166">The simplest is by using the `Task`'s [`Result` property](https://docs.microsoft.com/dotnet/api/system.threading.tasks.task-1.result):</span></span>

```csharp
    var res = BellTest.Run(sim, 1000, initial).Result;
```
<span data-ttu-id="d7236-167">mas outras técnicas, como usar o [método `Wait`](https://docs.microsoft.com/dotnet/api/system.threading.tasks.task.wait) ou a [palavra-chave `await`](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/await) do C# também funcionarão.</span><span class="sxs-lookup"><span data-stu-id="d7236-167">but other techniques, like using the [`Wait` method](https://docs.microsoft.com/dotnet/api/system.threading.tasks.task.wait) or C# [`await` keyword](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/await) will also work.</span></span>

<span data-ttu-id="d7236-168">Como acontece com argumentos, as tuplas Q# são representadas como instâncias de `ValueTuple` e as matrizes Q# são representadas como instâncias de `QArray`.</span><span class="sxs-lookup"><span data-stu-id="d7236-168">As with arguments, Q# tuples are represented as `ValueTuple` instances and Q# arrays are represented as `QArray` instances.</span></span>
<span data-ttu-id="d7236-169">Os tipos definidos pelo usuário são retornados como os tipos base.</span><span class="sxs-lookup"><span data-stu-id="d7236-169">User-defined types are returned as their base types.</span></span>
<span data-ttu-id="d7236-170">A tupla vazia, `()`, é retornada como uma instância da classe `QVoid`.</span><span class="sxs-lookup"><span data-stu-id="d7236-170">The empty tuple, `()`, is returned as an instance of the `QVoid` class.</span></span>

<span data-ttu-id="d7236-171">Muitos algoritmos quânticos exigem pós-processamento substancial para obter respostas úteis.</span><span class="sxs-lookup"><span data-stu-id="d7236-171">Many quantum algorithms require substantial post-processing to derive useful answers.</span></span>
<span data-ttu-id="d7236-172">Por exemplo, a parte quântica do algoritmo de Shor é apenas o início de uma computação que localiza os fatores de um número.</span><span class="sxs-lookup"><span data-stu-id="d7236-172">For instance, the quantum part of Shor's algorithm is just the beginning of a computation that finds the factors of a number.</span></span>

<span data-ttu-id="d7236-173">Na maioria dos casos, é mais simples e mais fácil fazer esse tipo de pós-processamento no driver clássico.</span><span class="sxs-lookup"><span data-stu-id="d7236-173">In most cases, it is simplest and easiest to do this sort of post-processing in the classical driver.</span></span>
<span data-ttu-id="d7236-174">Somente o driver clássico pode relatar resultados para o usuário ou gravá-los em disco.</span><span class="sxs-lookup"><span data-stu-id="d7236-174">Only the classical driver can report results to the user or write them to disk.</span></span>
<span data-ttu-id="d7236-175">O driver clássico terá acesso a bibliotecas analíticas e a outras funções matemáticas que não são expostas no Q#.</span><span class="sxs-lookup"><span data-stu-id="d7236-175">The classical driver will have access to analytical libraries and other mathematical functions that are not exposed in Q#.</span></span>


## <a name="failures"></a><span data-ttu-id="d7236-176">Falhas</span><span class="sxs-lookup"><span data-stu-id="d7236-176">Failures</span></span>

<span data-ttu-id="d7236-177">Quando a instrução `fail` Q# é atingida durante a execução de uma operação, uma `ExecutionFailException` é gerada.</span><span class="sxs-lookup"><span data-stu-id="d7236-177">When the Q# `fail` statement is reached during the execution of an operation, an `ExecutionFailException` is thrown.</span></span>

<span data-ttu-id="d7236-178">Devido ao uso de `System.Task` no método `Run`, a exceção gerada como resultado de uma instrução `fail` será encapsulada em uma `System.AggregateException`.</span><span class="sxs-lookup"><span data-stu-id="d7236-178">Due to the use of `System.Task` in the `Run` method, the exception thrown as a result of a `fail` statement will be wrapped into a `System.AggregateException`.</span></span>
<span data-ttu-id="d7236-179">Para encontrar o motivo real da falha, você precisará iterar no `AggregateException` 
`InnerExceptions`, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d7236-179">To find the actual reason for the failure, you need to iterate into the `AggregateException` 
`InnerExceptions`, for example:</span></span>

```csharp

            try
            {
                using(var sim = new QuantumSimulator())
                {
                    /// call your operations here...
                }
            }
            catch (AggregateException e)
            {
                // Unwrap AggregateException to get the message from Q# fail statement.
                // Go through all inner exceptions.
                foreach (Exception inner in e.InnerExceptions)
                {
                    // If the exception of type ExecutionFailException
                    if (inner is ExecutionFailException failException)
                    {
                        // Print the message it contains
                        Console.WriteLine($" {failException.Message}");
                    }
                }
            }
```

## <a name="other-classical-languages"></a><span data-ttu-id="d7236-180">Outras linguagens clássicas</span><span class="sxs-lookup"><span data-stu-id="d7236-180">Other Classical Languages</span></span>

<span data-ttu-id="d7236-181">Embora as amostras que fornecemos estejam em C#, F# e Python, o Quantum development kit também dá suporte à composição de programas host clássicos em outras linguagens.</span><span class="sxs-lookup"><span data-stu-id="d7236-181">While the samples we have provided are in C#, F#, and Python, the Quantum Development Kit also supports writing classical host programs in other languages.</span></span>
<span data-ttu-id="d7236-182">Por exemplo, se você quiser escrever um programa host no Visual Basic, [ele deverá funcionar corretamente](https://github.com/tcNickolas/MiscQSharp/blob/master/Quantum_VBNet/README.md#using-q-with-visual-basic-net).</span><span class="sxs-lookup"><span data-stu-id="d7236-182">For example, if you want to write a host program in Visual Basic, [it should work just fine](https://github.com/tcNickolas/MiscQSharp/blob/master/Quantum_VBNet/README.md#using-q-with-visual-basic-net).</span></span>
