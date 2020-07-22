---
title: Simulador de Quantum de estado completo – kit de desenvolvimento do Quantum
description: 'Saiba como executar seus programas do Q # no Microsoft Quantum Development Kit o simulador de estado completo.'
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 06/26/2020
ms.topic: article
uid: microsoft.quantum.machines.full-state-simulator
ms.openlocfilehash: 563fdbd2a45461d112e4c46651eddd75c6fc3db2
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871171"
---
# <a name="quantum-development-kit-qdk-full-state-simulator"></a><span data-ttu-id="37edd-103">Simulador de estado completo do QDK (Kit de desenvolvimento do Quantum)</span><span class="sxs-lookup"><span data-stu-id="37edd-103">Quantum Development Kit (QDK) full state simulator</span></span>

<span data-ttu-id="37edd-104">O QDK fornece um simulador de estado completo que simula um computador Quantum em seu computador local.</span><span class="sxs-lookup"><span data-stu-id="37edd-104">The QDK provides a full state simulator that simulates a quantum machine on your local computer.</span></span> <span data-ttu-id="37edd-105">Você pode usar o simulador de estado completo para executar e depurar algoritmos de Quantum escritos em Q #, utilizando até 30 qubits.</span><span class="sxs-lookup"><span data-stu-id="37edd-105">You can use the full state simulator to run and debug quantum algorithms written in Q#, utilizing up to 30 qubits.</span></span> <span data-ttu-id="37edd-106">O simulador de estado completo é semelhante ao simulador do Quantum usado na [interface do usuário do Liq $ | \rangle $](http://stationq.github.io/Liquid/) da Microsoft Research.</span><span class="sxs-lookup"><span data-stu-id="37edd-106">The full state simulator is similar to the quantum simulator used in the  [LIQ$Ui|\rangle$](http://stationq.github.io/Liquid/) platform from Microsoft Research.</span></span>

## <a name="invoking-and-running-the-full-state-simulator"></a><span data-ttu-id="37edd-107">Invocando e executando o simulador de estado completo</span><span class="sxs-lookup"><span data-stu-id="37edd-107">Invoking and running the full state simulator</span></span>

<span data-ttu-id="37edd-108">Você expõe o simulador de estado completo por meio da `QuantumSimulator` classe.</span><span class="sxs-lookup"><span data-stu-id="37edd-108">You expose the full state simulator via the `QuantumSimulator` class.</span></span> <span data-ttu-id="37edd-109">Para obter detalhes adicionais, consulte [maneiras de executar um programa Q #](xref:microsoft.quantum.guide.host-programs).</span><span class="sxs-lookup"><span data-stu-id="37edd-109">For additional details, see [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>

### <a name="invoking-the-simulator-from-c"></a><span data-ttu-id="37edd-110">Invocando o simulador a partir de C #</span><span class="sxs-lookup"><span data-stu-id="37edd-110">Invoking the simulator from C#</span></span>

<span data-ttu-id="37edd-111">Crie uma instância da `QuantumSimulator` classe e, em seguida, passe-a para o `Run` método de uma operação Quantum, juntamente com quaisquer parâmetros adicionais.</span><span class="sxs-lookup"><span data-stu-id="37edd-111">Create an instance of the `QuantumSimulator` class and then pass it to the `Run` method of a quantum operation, along with any additional parameters.</span></span>
```csharp
    using (var sim = new QuantumSimulator())
    {
        var res = myOperation.Run(sim).Result;
        ///...
    }
```

<span data-ttu-id="37edd-112">Como a `QuantumSimulator` classe implementa a <xref:System.IDisposable> interface, você deve chamar o `Dispose` método assim que não precisar mais da instância do simulador.</span><span class="sxs-lookup"><span data-stu-id="37edd-112">Because the `QuantumSimulator` class implements the <xref:System.IDisposable> interface, you must call the `Dispose` method once you do not need the instance of the simulator anymore.</span></span> <span data-ttu-id="37edd-113">A melhor maneira de fazer isso é encapsular a declaração de simulador e as operações em uma instrução [using](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/using-statement) , que chama automaticamente o `Dispose` método.</span><span class="sxs-lookup"><span data-stu-id="37edd-113">The best way to do this is to wrap the simulator declaration and operations within a [using](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/using-statement) statement, which automatically calls the `Dispose` method.</span></span>

### <a name="invoking-the-simulator-from-python"></a><span data-ttu-id="37edd-114">Invocando o simulador do Python</span><span class="sxs-lookup"><span data-stu-id="37edd-114">Invoking the simulator from Python</span></span>

<span data-ttu-id="37edd-115">Use o método [simular ()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) da biblioteca do Python q # com a operação de q # importada:</span><span class="sxs-lookup"><span data-stu-id="37edd-115">Use the [simulate()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) method from the Q# Python library with the imported Q# operation:</span></span>

```python
qubit_result = myOperation.simulate()
```

### <a name="invoking-the-simulator-from-the-command-line"></a><span data-ttu-id="37edd-116">Invocando o simulador a partir da linha de comando</span><span class="sxs-lookup"><span data-stu-id="37edd-116">Invoking the simulator from the command line</span></span>

<span data-ttu-id="37edd-117">Ao executar um programa Q # da linha de comando, o simulador de estado completo é o computador de destino padrão.</span><span class="sxs-lookup"><span data-stu-id="37edd-117">When running a Q# program from the command line, the full state simulator is the default target machine.</span></span> <span data-ttu-id="37edd-118">Opcionalmente, você pode usar o parâmetro **--Simulator** (ou **-s** Shortcut) para especificar o computador de destino desejado.</span><span class="sxs-lookup"><span data-stu-id="37edd-118">Optionally, you can use the **--simulator** (or **-s** shortcut) parameter to specify the desired target machine.</span></span> <span data-ttu-id="37edd-119">Ambos os comandos a seguir executam um programa usando o simulador de estado completo.</span><span class="sxs-lookup"><span data-stu-id="37edd-119">Both of the following commands run a program using the full state simulator.</span></span> 

```dotnetcli
dotnet run
dotnet run -s QuantumSimulator
```

### <a name="invoking-the-simulator-from-juptyer-notebooks"></a><span data-ttu-id="37edd-120">Invocando o simulador de notebooks Juptyer</span><span class="sxs-lookup"><span data-stu-id="37edd-120">Invoking the simulator from Juptyer Notebooks</span></span>

<span data-ttu-id="37edd-121">Use o comando do QI # mágico [% simular](xref:microsoft.quantum.iqsharp.magic-ref.simulate) para executar a operação Q #.</span><span class="sxs-lookup"><span data-stu-id="37edd-121">Use the IQ# magic command [%simulate](xref:microsoft.quantum.iqsharp.magic-ref.simulate) to run the Q# operation.</span></span>

```
%simulate myOperation
```
## <a name="seeding-the-simulator"></a><span data-ttu-id="37edd-122">Propagando o simulador</span><span class="sxs-lookup"><span data-stu-id="37edd-122">Seeding the simulator</span></span>

<span data-ttu-id="37edd-123">Por padrão, o simulador de estado completo usa um gerador de número aleatório para simular a aleatoriedade Quantum.</span><span class="sxs-lookup"><span data-stu-id="37edd-123">By default, the full state simulator uses a random number generator to simulate quantum randomness.</span></span> <span data-ttu-id="37edd-124">Para fins de teste, às vezes é útil ter resultados determinísticos.</span><span class="sxs-lookup"><span data-stu-id="37edd-124">For testing purposes, it is sometimes useful to have deterministic results.</span></span> <span data-ttu-id="37edd-125">Em um programa em C#, você pode fazer isso fornecendo uma semente para o gerador de números aleatórios no `QuantumSimulator` Construtor por meio do `randomNumberGeneratorSeed` parâmetro.</span><span class="sxs-lookup"><span data-stu-id="37edd-125">In a C# program, you can accomplish this by providing a seed for the random number generator in the `QuantumSimulator` constructor via the `randomNumberGeneratorSeed` parameter.</span></span>

```csharp
    using (var sim = new QuantumSimulator(randomNumberGeneratorSeed: 42))
    {
        var res = myOperationTest.Run(sim).Result;
        ///...
    }
```

## <a name="configuring-threads"></a><span data-ttu-id="37edd-126">Configurando threads</span><span class="sxs-lookup"><span data-stu-id="37edd-126">Configuring threads</span></span>

<span data-ttu-id="37edd-127">O simulador de estado completo usa [OpenMP](http://www.openmp.org/) para paralelizar a Algebra linear necessária.</span><span class="sxs-lookup"><span data-stu-id="37edd-127">The full state simulator uses [OpenMP](http://www.openmp.org/) to parallelize the linear algebra required.</span></span> <span data-ttu-id="37edd-128">Por padrão, o OpenMP usa todos os threads de hardware disponíveis, o que significa que programas com pequenos números de qubits geralmente são executados lentamente porque a coordenação necessária Dwarfs o trabalho real.</span><span class="sxs-lookup"><span data-stu-id="37edd-128">By default, OpenMP uses all available hardware threads, which means that programs with small numbers of qubits often runs slowly because the coordination that is required dwarfs the actual work.</span></span> <span data-ttu-id="37edd-129">Você pode corrigir isso definindo a variável de ambiente `OMP_NUM_THREADS` para um número pequeno.</span><span class="sxs-lookup"><span data-stu-id="37edd-129">You can fix this by setting the environment variable `OMP_NUM_THREADS` to a small number.</span></span> <span data-ttu-id="37edd-130">Como regra prática, configure um thread para até quatro qubits e, em seguida, um thread adicional por qubit.</span><span class="sxs-lookup"><span data-stu-id="37edd-130">As a rule of thumb, configure one thread for up to four qubits, and then one additional thread per qubit.</span></span> <span data-ttu-id="37edd-131">Talvez seja necessário ajustar a variável dependendo do algoritmo.</span><span class="sxs-lookup"><span data-stu-id="37edd-131">You might need to adjust the variable depending on your algorithm.</span></span>

## <a name="see-also"></a><span data-ttu-id="37edd-132">Veja também</span><span class="sxs-lookup"><span data-stu-id="37edd-132">See also</span></span>

- [<span data-ttu-id="37edd-133">Estimador de recursos Quantum</span><span class="sxs-lookup"><span data-stu-id="37edd-133">Quantum resources estimator</span></span>](xref:microsoft.quantum.machines.resources-estimator)
- [<span data-ttu-id="37edd-134">Simulador de Toffoli Quantum</span><span class="sxs-lookup"><span data-stu-id="37edd-134">Quantum Toffoli simulator</span></span>](xref:microsoft.quantum.machines.toffoli-simulator)
- [<span data-ttu-id="37edd-135">Simulador de rastreamento Quantum</span><span class="sxs-lookup"><span data-stu-id="37edd-135">Quantum trace simulator</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.intro)