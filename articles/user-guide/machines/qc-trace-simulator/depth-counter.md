---
title: Contador de profundidade – kit de desenvolvimento do Quantum
description: Saiba mais sobre o contador de profundidade do Microsoft QDK, que usa o simulador de rastreamento do Quantum para reunir contagens da profundidade de cada operação invocada em um Q# programa.
author: vadym-kl
ms.author: vadym
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.depth-counter
no-loc:
- Q#
- $$v
ms.openlocfilehash: 8280783adfcc2867c3a598a6f57d827125aadcfd
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90833441"
---
# <a name="quantum-trace-simulator-depth-counter"></a><span data-ttu-id="fa28e-103">Simulador de rastreamento Quantum: contador de profundidade</span><span class="sxs-lookup"><span data-stu-id="fa28e-103">Quantum trace simulator: depth counter</span></span>

<span data-ttu-id="fa28e-104">O contador de profundidade faz parte do [simulador de rastreamento Quantum](xref:microsoft.quantum.machines.qc-trace-simulator.intro)do kit de desenvolvimento Quantum.</span><span class="sxs-lookup"><span data-stu-id="fa28e-104">The depth counter is a part of the Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span>
<span data-ttu-id="fa28e-105">Você pode usá-lo para reunir contagens que representam o limite inferior da profundidade de cada operação invocada em um programa Quantum.</span><span class="sxs-lookup"><span data-stu-id="fa28e-105">You can use it to gather counts that represent the lower bound of the depth of every operation invoked in a quantum program.</span></span> 

## <a name="depth-values"></a><span data-ttu-id="fa28e-106">Valores de profundidade</span><span class="sxs-lookup"><span data-stu-id="fa28e-106">Depth values</span></span>

<span data-ttu-id="fa28e-107">Por padrão, todas as operações têm uma profundidade de **0** , exceto a `T` operação, que tem uma profundidade de **1**.</span><span class="sxs-lookup"><span data-stu-id="fa28e-107">By default, all operations have a depth of **0** except the `T` operation, which has a depth of **1**.</span></span> <span data-ttu-id="fa28e-108">Isso significa que, por padrão, apenas a `T` profundidade das operações é computada (o que geralmente é desejável).</span><span class="sxs-lookup"><span data-stu-id="fa28e-108">This means that by default, only the `T` depth of operations is computed (which is often desirable).</span></span> <span data-ttu-id="fa28e-109">O contador de profundidade agrega e coleta estatísticas sobre todas as bordas do [grafo de chamada](https://en.wikipedia.org/wiki/Call_graph)da operação.</span><span class="sxs-lookup"><span data-stu-id="fa28e-109">The depth counter aggregates and collects statistics over all the edges of the operation's [call graph](https://en.wikipedia.org/wiki/Call_graph).</span></span>

<span data-ttu-id="fa28e-110">Todas as <xref:microsoft.quantum.intrinsic> operações são expressas em termos de rotações de qubit único, operações <xref:microsoft.quantum.intrinsic.t> , operações de Clifford de qubit único, <xref:microsoft.quantum.intrinsic.cnot> operações e medidas de Pauli de vários qubit observáveis.</span><span class="sxs-lookup"><span data-stu-id="fa28e-110">All <xref:microsoft.quantum.intrinsic> operations are expressed in terms of single-qubit rotations, <xref:microsoft.quantum.intrinsic.t> operations, single-qubit Clifford operations, <xref:microsoft.quantum.intrinsic.cnot> operations, and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="fa28e-111">Os usuários podem definir a profundidade para cada uma das operações primitivas por meio do `gateTimes` campo de <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> .</span><span class="sxs-lookup"><span data-stu-id="fa28e-111">Users can set the depth for each of the primitive operations via the `gateTimes` field of <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>.</span></span>

## <a name="invoking-the-depth-counter"></a><span data-ttu-id="fa28e-112">Invocando o contador de profundidade</span><span class="sxs-lookup"><span data-stu-id="fa28e-112">Invoking the depth counter</span></span>

<span data-ttu-id="fa28e-113">Para executar o simulador de rastreamento Quantum com o contador de profundidade, você deve criar uma <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instância, definir sua `UseDepthCounter` propriedade como **true**e, em seguida, criar uma nova <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instância com `QCTraceSimulatorConfiguration` como o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="fa28e-113">To run the quantum trace simulator with the depth counter, you must create a <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instance, set its `UseDepthCounter` property to **true**, and then create a new <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instance with `QCTraceSimulatorConfiguration` as the parameter.</span></span> 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseDepthCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-depth-counter-in-a-c-host-program"></a><span data-ttu-id="fa28e-114">Usando o contador de profundidade em um programa de host C#</span><span class="sxs-lookup"><span data-stu-id="fa28e-114">Using the depth counter in a C# host program</span></span>

<span data-ttu-id="fa28e-115">O exemplo de C# a seguir nesta seção computa a `T` profundidade da `CCNOT` operação, com base no seguinte código de Q# exemplo:</span><span class="sxs-lookup"><span data-stu-id="fa28e-115">The C# example that follows in this section computes the `T` depth of the `CCNOT` operation, based on the following Q# sample code:</span></span>

```qsharp
open Microsoft.Quantum.Intrinsic;

operation ApplySampleWithCCNOT() : Unit {
    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

<span data-ttu-id="fa28e-116">Para verificar se `CCNOT` `T` o tem profundidade **5** e `ApplySampleWithCCNOT` tem `T` profundidade **6**, use o seguinte código C#:</span><span class="sxs-lookup"><span data-stu-id="fa28e-116">To check that `CCNOT` has `T` depth **5** and `ApplySampleWithCCNOT` has `T` depth **6**, use the following C# code:</span></span>

```csharp
using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.UseDepthCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tDepth = sim.GetMetric<Intrinsic.CCNOT, ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
```

<span data-ttu-id="fa28e-117">A primeira parte do programa é executada `ApplySampleWithCCNOT` .</span><span class="sxs-lookup"><span data-stu-id="fa28e-117">The first part of the program runs `ApplySampleWithCCNOT`.</span></span> <span data-ttu-id="fa28e-118">A segunda parte usa o [`GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) método para recuperar a `T` profundidade de `CCNOT` e `ApplySampleWithCCNOT` .</span><span class="sxs-lookup"><span data-stu-id="fa28e-118">The second part uses the [`GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) method to retrieve the `T` depth of `CCNOT` and `ApplySampleWithCCNOT`.</span></span> 

<span data-ttu-id="fa28e-119">Por fim, você pode gerar todas as estatísticas coletadas pelo contador de profundidade no formato CSV usando o seguinte:</span><span class="sxs-lookup"><span data-stu-id="fa28e-119">Finally, you can output all the statistics collected by the depth counter in CSV format using the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.depthCounter];
```

## <a name="see-also"></a><span data-ttu-id="fa28e-120">Consulte também</span><span class="sxs-lookup"><span data-stu-id="fa28e-120">See also</span></span>

- <span data-ttu-id="fa28e-121">A visão geral do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro) do quantum do kit de desenvolvimento Quantum.</span><span class="sxs-lookup"><span data-stu-id="fa28e-121">The Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
- <span data-ttu-id="fa28e-122">A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> referência da API.</span><span class="sxs-lookup"><span data-stu-id="fa28e-122">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API reference.</span></span>
- <span data-ttu-id="fa28e-123">A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> referência da API.</span><span class="sxs-lookup"><span data-stu-id="fa28e-123">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API reference.</span></span>
- <span data-ttu-id="fa28e-124">A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.DepthCounter> referência da API.</span><span class="sxs-lookup"><span data-stu-id="fa28e-124">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.DepthCounter> API reference.</span></span>
