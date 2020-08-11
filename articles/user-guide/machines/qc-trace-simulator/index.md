---
title: Simulador de rastreamento quântico – Quantum Development Kit
description: Aprenda a usar o simulador de rastreamento do computador quântico da Microsoft para depurar código clássico e estimar os requisitos de recursos de um programa Q#.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.intro
no-loc:
- Q#
- $$v
ms.openlocfilehash: 5d5efef037ff236bd040dfd88e94f7f3dd331aef
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868212"
---
# <a name="microsoft-quantum-development-kit-qdk-quantum-trace-simulator"></a><span data-ttu-id="a421e-103">Simulador de rastreamento quântico do Microsoft QDK (Quantum Development Kit)</span><span class="sxs-lookup"><span data-stu-id="a421e-103">Microsoft Quantum Development Kit (QDK) quantum trace simulator</span></span>

<span data-ttu-id="a421e-104">A classe QDK <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> executa um programa quântico sem realmente simular o estado de um computador quântico.</span><span class="sxs-lookup"><span data-stu-id="a421e-104">The QDK <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> class runs a quantum program without actually simulating the state of a quantum computer.</span></span> <span data-ttu-id="a421e-105">Por esse motivo, o simulador de rastreamento quântico pode executar programas quânticos que usam milhares de qubits.</span><span class="sxs-lookup"><span data-stu-id="a421e-105">For this reason, the quantum trace simulator is able to run quantum programs that use thousands of qubits.</span></span>  <span data-ttu-id="a421e-106">Ele é útil para duas finalidades principais:</span><span class="sxs-lookup"><span data-stu-id="a421e-106">It is useful for two main purposes:</span></span> 

* <span data-ttu-id="a421e-107">Depuração de código clássico que faça parte de um programa quântico.</span><span class="sxs-lookup"><span data-stu-id="a421e-107">Debugging classical code that is part of a quantum program.</span></span> 
* <span data-ttu-id="a421e-108">Estimativa dos recursos necessários para executar determinada instância de um programa quântico em um computador quântico.</span><span class="sxs-lookup"><span data-stu-id="a421e-108">Estimating the resources required to run a given instance of a quantum program on a quantum computer.</span></span> <span data-ttu-id="a421e-109">Na verdade, o [Avaliador de recursos](xref:microsoft.quantum.machines.resources-estimator), que fornece um conjunto mais limitado de métricas, é criado com base no simulador de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="a421e-109">In fact, the [Resources estimator](xref:microsoft.quantum.machines.resources-estimator), which provides a more limited set of metrics, is built upon the trace simulator.</span></span>

## <a name="invoking-the-quantum-trace-simulator"></a><span data-ttu-id="a421e-110">Invocando o simulador de rastreamento quântico</span><span class="sxs-lookup"><span data-stu-id="a421e-110">Invoking the quantum trace simulator</span></span>

<span data-ttu-id="a421e-111">É possível usar o simulador de rastreamento quântico para executar qualquer operação Q#.</span><span class="sxs-lookup"><span data-stu-id="a421e-111">You can use the quantum trace simulator to run any Q# operation.</span></span>

<span data-ttu-id="a421e-112">Assim como acontece com outros computadores de destino, primeiramente você cria uma instância da classe `QCTraceSimulator` e, em seguida, passa-a como o primeiro parâmetro do método `Run` de uma operação.</span><span class="sxs-lookup"><span data-stu-id="a421e-112">As with other target machines, you first create an instance of the `QCTraceSimulator` class and then pass it as the first parameter of an operation's `Run` method.</span></span>

<span data-ttu-id="a421e-113">Observe que, diferentemente da classe `QuantumSimulator`, a classe `QCTraceSimulator` não implementa a interface <xref:System.IDisposable> e, portanto, você não precisa colocá-la em uma instrução `using`.</span><span class="sxs-lookup"><span data-stu-id="a421e-113">Note that, unlike the `QuantumSimulator` class, the `QCTraceSimulator` class does not implement the <xref:System.IDisposable> interface, and thus you do not need to enclose it within a `using` statement.</span></span>

```csharp
using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;
using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;

namespace Quantum.MyProgram
{
    class Driver
    {
        static void Main(string[] args)
        {
            QCTraceSimulator sim = new QCTraceSimulator();
            var res = MyQuantumProgram.Run(sim).Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

## <a name="providing-the-probability-of-measurement-outcomes"></a><span data-ttu-id="a421e-114">Como fornecer a probabilidade de resultados de medida</span><span class="sxs-lookup"><span data-stu-id="a421e-114">Providing the probability of measurement outcomes</span></span>

<span data-ttu-id="a421e-115">Como o simulador de rastreamento quântico não simula o estado real quântico, ele não pode calcular a probabilidade de resultados de medida em uma operação.</span><span class="sxs-lookup"><span data-stu-id="a421e-115">Because the quantum trace simulator does not simulate the actual quantum state, it cannot calculate the probability of measurement outcomes within an operation.</span></span> 

<span data-ttu-id="a421e-116">Portanto, se uma operação incluir medidas, você precisará fornecer explicitamente essas probabilidades usando a operação <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> do namespace <xref:microsoft.quantum.diagnostics>.</span><span class="sxs-lookup"><span data-stu-id="a421e-116">Therefore, if an operation includes measurements, you must explicitly provide these probabilities using the <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> operation from the <xref:microsoft.quantum.diagnostics> namespace.</span></span> <span data-ttu-id="a421e-117">O exemplo a seguir ilustra isso:</span><span class="sxs-lookup"><span data-stu-id="a421e-117">The following example illustrates this:</span></span>

```qsharp
operation TeleportQubit(source : Qubit, target : Qubit) : Unit {
    using (qubit = Qubit()) {
        H(qubit);
        CNOT(qubit, target);
        CNOT(source, qubit);
        H(source);

        AssertMeasurementProbability([PauliZ], [source], Zero, 0.5, "Outcomes must be equally likely", 1e-5);
        AssertMeasurementProbability([PauliZ], [q], Zero, 0.5, "Outcomes must be equally likely", 1e-5);

        if (M(source) == One)  { Z(target); X(source); }
        if (M(q) == One) { X(target); X(q); }
    }
}
```

<span data-ttu-id="a421e-118">Quando o simulador de rastreamento quântico executar `AssertMeasurementProbability`, ele registrará isso medindo `PauliZ` em `source` e `q` deverá mostrar um resultado igual a `Zero` com a probabilidade de **0,5**.</span><span class="sxs-lookup"><span data-stu-id="a421e-118">When the quantum trace simulator encounters `AssertMeasurementProbability` it records that measuring `PauliZ` on `source` and `q` should give an outcome of `Zero`, with probability **0.5**.</span></span> <span data-ttu-id="a421e-119">Quando ele executar a operação `M` posteriormente, ele localizará os valores gravados das probabilidades de resultado e `M` retornará `Zero` ou `One`, com a probabilidade de **0,5**.</span><span class="sxs-lookup"><span data-stu-id="a421e-119">When it runs the `M` operation later, it finds the recorded values of the outcome probabilities, and `M` returns `Zero` or `One`, with probability **0.5**.</span></span> <span data-ttu-id="a421e-120">Quando o mesmo código for executado em um simulador que controla o estado quântico, esse simulador verificará se as probabilidades fornecidas em `AssertMeasurementProbability` estão corretas.</span><span class="sxs-lookup"><span data-stu-id="a421e-120">When the same code runs on a simulator that keeps track of the quantum state, that simulator checks that the provided probabilities in `AssertMeasurementProbability` are correct.</span></span>

<span data-ttu-id="a421e-121">Observe que, se houver pelo menos uma operação de medida que não está anotada usando `AssertMeasurementProbability`, o simulador gerará um [`UnconstrainedMeasurementException`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.unconstrainedmeasurementexception).</span><span class="sxs-lookup"><span data-stu-id="a421e-121">Note that if there is at least one measurement operation that is not annotated using `AssertMeasurementProbability`, the simulator throws an [`UnconstrainedMeasurementException`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.unconstrainedmeasurementexception).</span></span>

## <a name="quantum-trace-simulator-tools"></a><span data-ttu-id="a421e-122">Ferramentas de simulador de rastreamento quântico</span><span class="sxs-lookup"><span data-stu-id="a421e-122">Quantum trace simulator tools</span></span>

<span data-ttu-id="a421e-123">O QDK inclui cinco ferramentas que você pode usar com o simulador de rastreamento quântico para detectar bugs nos seus programas e executar estimativas de recursos do programa quântico:</span><span class="sxs-lookup"><span data-stu-id="a421e-123">The QDK includes five tools that you can use with the quantum trace simulator to detect bugs in your programs and perform quantum program resource estimates:</span></span> 

|<span data-ttu-id="a421e-124">Ferramenta</span><span class="sxs-lookup"><span data-stu-id="a421e-124">Tool</span></span> | <span data-ttu-id="a421e-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="a421e-125">Description</span></span> |
|-----| -----|
|[<span data-ttu-id="a421e-126">Verificador de entradas distintas</span><span class="sxs-lookup"><span data-stu-id="a421e-126">Distinct inputs checker</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs) |<span data-ttu-id="a421e-127">Verifica se há conflitos potenciais com qubits compartilhados</span><span class="sxs-lookup"><span data-stu-id="a421e-127">Checks for potential conflicts with shared qubits</span></span> |
|[<span data-ttu-id="a421e-128">Verificador de uso de qubits invalidados</span><span class="sxs-lookup"><span data-stu-id="a421e-128">Invalidated qubits use checker</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits)  |<span data-ttu-id="a421e-129">Verifica se o programa aplica uma operação a um qubit que já foi liberado</span><span class="sxs-lookup"><span data-stu-id="a421e-129">Checks if the program applies an operation to a qubit that is already released</span></span> |
|[<span data-ttu-id="a421e-130">Contador de operações primitivas</span><span class="sxs-lookup"><span data-stu-id="a421e-130">Primitive operations counter</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter)  | <span data-ttu-id="a421e-131">Conta o número de execuções primitivas usadas em cada operação invocada em um programa quântico</span><span class="sxs-lookup"><span data-stu-id="a421e-131">Counts the number of primitive executions used by every operation invoked in a quantum program</span></span>  |
|[<span data-ttu-id="a421e-132">Contador de profundidade</span><span class="sxs-lookup"><span data-stu-id="a421e-132">Depth counter</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter)  |<span data-ttu-id="a421e-133">Coleta contagens que representam o limite inferior da profundidade de cada operação invocada em um programa quântico</span><span class="sxs-lookup"><span data-stu-id="a421e-133">Gathers counts that represent the lower bound of the depth of every operation invoked in a quantum program</span></span>   |
|[<span data-ttu-id="a421e-134">Contador de largura</span><span class="sxs-lookup"><span data-stu-id="a421e-134">Width counter</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter)  |<span data-ttu-id="a421e-135">Conta o número de qubits alocados e emprestados em cada operação em um programa quântico</span><span class="sxs-lookup"><span data-stu-id="a421e-135">Counts the number of qubits allocated and borrowed by each operation in a quantum program</span></span> |

<span data-ttu-id="a421e-136">Cada uma dessas ferramentas é habilitada definindo sinalizadores apropriados no `QCTraceSimulatorConfiguration` e, em seguida, passando a configuração para a declaração de `QCTraceSimulator`.</span><span class="sxs-lookup"><span data-stu-id="a421e-136">Each of these tools is enabled by setting appropriate flags in `QCTraceSimulatorConfiguration` and then passing the configuration to the `QCTraceSimulator` declaration.</span></span> <span data-ttu-id="a421e-137">Para obter informações sobre como usar cada uma dessas ferramentas, confira os links na lista anterior.</span><span class="sxs-lookup"><span data-stu-id="a421e-137">For information on using each of these tools, see the links in the preceding list.</span></span> <span data-ttu-id="a421e-138">Para obter mais informações sobre como configurar o `QCTraceSimulator`, confira [QCTraceSimulatorConfiguration](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration).</span><span class="sxs-lookup"><span data-stu-id="a421e-138">For more information about configuring `QCTraceSimulator`, see [QCTraceSimulatorConfiguration](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration).</span></span>

## <a name="qctracesimulator-methods"></a><span data-ttu-id="a421e-139">Métodos QCTraceSimulator</span><span class="sxs-lookup"><span data-stu-id="a421e-139">QCTraceSimulator methods</span></span>

<span data-ttu-id="a421e-140">O `QCTraceSimulator` tem vários métodos internos para recuperar os valores das métricas rastreadas durante uma operação quântica.</span><span class="sxs-lookup"><span data-stu-id="a421e-140">`QCTraceSimulator` has several built-in methods to retrieve the values of the metrics tracked during a quantum operation.</span></span> <span data-ttu-id="a421e-141">Exemplos dos métodos [QCTraceSimulator.GetMetric](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) e [QCTraceSimulator.ToCSV](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.tocsv) podem ser encontrados nos artigos [Contador de operações primitivo](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter), [Contador de profundidade](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) e [Contador de largura](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter).</span><span class="sxs-lookup"><span data-stu-id="a421e-141">Examples of the [QCTraceSimulator.GetMetric](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) and the [QCTraceSimulator.ToCSV](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.tocsv) methods can be found in the [Primitive operations counter](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter), [Depth counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter), and [Width counter](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter) articles.</span></span> <span data-ttu-id="a421e-142">Para saber mais sobre todos os métodos disponíveis, confira [QCTraceSimulator](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) na referência da API do Q#.</span><span class="sxs-lookup"><span data-stu-id="a421e-142">For more information on all available methods, see [QCTraceSimulator](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) in the Q# API reference.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a421e-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="a421e-143">See also</span></span>

- [<span data-ttu-id="a421e-144">Avaliador de recursos quânticos</span><span class="sxs-lookup"><span data-stu-id="a421e-144">Quantum resources estimator</span></span>](xref:microsoft.quantum.machines.resources-estimator)
- [<span data-ttu-id="a421e-145">Simulador quântico do Toffoli</span><span class="sxs-lookup"><span data-stu-id="a421e-145">Quantum Toffoli simulator</span></span>](xref:microsoft.quantum.machines.toffoli-simulator)
- [<span data-ttu-id="a421e-146">Simulador de estado completo quântico</span><span class="sxs-lookup"><span data-stu-id="a421e-146">Quantum full state simulator</span></span>](xref:microsoft.quantum.machines.full-state-simulator) 