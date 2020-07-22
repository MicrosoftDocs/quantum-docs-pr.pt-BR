---
title: Contador de profundidade – kit de desenvolvimento do Quantum
description: 'Saiba mais sobre o contador de profundidade do Microsoft QDK, que usa o simulador de rastreamento do Quantum para reunir contagens da profundidade de cada operação invocada em um programa Q #.'
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.depth-counter
ms.openlocfilehash: 811e387fedf547d2681518ae0bb525c13dc84ff4
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871120"
---
# <a name="quantum-trace-simulator-depth-counter"></a><span data-ttu-id="256d2-103">Simulador de rastreamento Quantum: contador de profundidade</span><span class="sxs-lookup"><span data-stu-id="256d2-103">Quantum trace simulator: depth counter</span></span>

<span data-ttu-id="256d2-104">O contador de profundidade faz parte do [simulador de rastreamento Quantum](xref:microsoft.quantum.machines.qc-trace-simulator.intro)do kit de desenvolvimento Quantum.</span><span class="sxs-lookup"><span data-stu-id="256d2-104">The depth counter is a part of the Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span>
<span data-ttu-id="256d2-105">Você pode usá-lo para reunir contagens que representam o limite inferior da profundidade de cada operação invocada em um programa Quantum.</span><span class="sxs-lookup"><span data-stu-id="256d2-105">You can use it to gather counts that represent the lower bound of the depth of every operation invoked in a quantum program.</span></span> 

## <a name="depth-values"></a><span data-ttu-id="256d2-106">Valores de profundidade</span><span class="sxs-lookup"><span data-stu-id="256d2-106">Depth values</span></span>

<span data-ttu-id="256d2-107">Por padrão, todas as operações têm uma profundidade de **0** , exceto a `T` operação, que tem uma profundidade de **1**.</span><span class="sxs-lookup"><span data-stu-id="256d2-107">By default, all operations have a depth of **0** except the `T` operation, which has a depth of **1**.</span></span> <span data-ttu-id="256d2-108">Isso significa que, por padrão, apenas a `T` profundidade das operações é computada (o que geralmente é desejável).</span><span class="sxs-lookup"><span data-stu-id="256d2-108">This means that by default, only the `T` depth of operations is computed (which is often desirable).</span></span> <span data-ttu-id="256d2-109">O contador de profundidade agrega e coleta estatísticas sobre todas as bordas do [grafo de chamada](https://en.wikipedia.org/wiki/Call_graph)da operação.</span><span class="sxs-lookup"><span data-stu-id="256d2-109">The depth counter aggregates and collects statistics over all the edges of the operation's [call graph](https://en.wikipedia.org/wiki/Call_graph).</span></span>

<span data-ttu-id="256d2-110">Todas as <xref:microsoft.quantum.intrinsic> operações são expressas em termos de rotações de qubit único, operações <xref:microsoft.quantum.intrinsic.t> , operações de Clifford de qubit único, <xref:microsoft.quantum.intrinsic.cnot> operações e medidas de Pauli de vários qubit observáveis.</span><span class="sxs-lookup"><span data-stu-id="256d2-110">All <xref:microsoft.quantum.intrinsic> operations are expressed in terms of single-qubit rotations, <xref:microsoft.quantum.intrinsic.t> operations, single-qubit Clifford operations, <xref:microsoft.quantum.intrinsic.cnot> operations, and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="256d2-111">Os usuários podem definir a profundidade para cada uma das operações primitivas por meio do `gateTimes` campo de <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> .</span><span class="sxs-lookup"><span data-stu-id="256d2-111">Users can set the depth for each of the primitive operations via the `gateTimes` field of <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>.</span></span>

## <a name="invoking-the-depth-counter"></a><span data-ttu-id="256d2-112">Invocando o contador de profundidade</span><span class="sxs-lookup"><span data-stu-id="256d2-112">Invoking the depth counter</span></span>

<span data-ttu-id="256d2-113">Para executar o simulador de rastreamento Quantum com o contador de profundidade, você deve criar uma <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instância, definir sua `UseDepthCounter` propriedade como **true**e, em seguida, criar uma nova <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instância com `QCTraceSimulatorConfiguration` como o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="256d2-113">To run the quantum trace simulator with the depth counter, you must create a <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instance, set its `UseDepthCounter` property to **true**, and then create a new <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instance with `QCTraceSimulatorConfiguration` as the parameter.</span></span> 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseDepthCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-depth-counter-in-a-c-host-program"></a><span data-ttu-id="256d2-114">Usando o contador de profundidade em um programa de host C#</span><span class="sxs-lookup"><span data-stu-id="256d2-114">Using the depth counter in a C# host program</span></span>

<span data-ttu-id="256d2-115">O exemplo de C# a seguir nesta seção computa a `T` profundidade da `CCNOT` operação, com base no seguinte código de exemplo de Q #:</span><span class="sxs-lookup"><span data-stu-id="256d2-115">The C# example that follows in this section computes the `T` depth of the `CCNOT` operation, based on the following Q# sample code:</span></span>

```qsharp
open Microsoft.Quantum.Intrinsic;

operation ApplySampleWithCCNOT() : Unit {
    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

<span data-ttu-id="256d2-116">Para verificar se `CCNOT` `T` o tem profundidade **5** e `ApplySampleWithCCNOT` tem `T` profundidade **6**, use o seguinte código C#:</span><span class="sxs-lookup"><span data-stu-id="256d2-116">To check that `CCNOT` has `T` depth **5** and `ApplySampleWithCCNOT` has `T` depth **6**, use the following C# code:</span></span>

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

<span data-ttu-id="256d2-117">A primeira parte do programa é executada `ApplySampleWithCCNOT` .</span><span class="sxs-lookup"><span data-stu-id="256d2-117">The first part of the program runs `ApplySampleWithCCNOT`.</span></span> <span data-ttu-id="256d2-118">A segunda parte usa o [`GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) método para recuperar a `T` profundidade de `CCNOT` e `ApplySampleWithCCNOT` .</span><span class="sxs-lookup"><span data-stu-id="256d2-118">The second part uses the [`GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) method to retrieve the `T` depth of `CCNOT` and `ApplySampleWithCCNOT`.</span></span> 

<span data-ttu-id="256d2-119">Por fim, você pode gerar todas as estatísticas coletadas pelo contador de profundidade no formato CSV usando o seguinte:</span><span class="sxs-lookup"><span data-stu-id="256d2-119">Finally, you can output all the statistics collected by the depth counter in CSV format using the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.depthCounter];
```

## <a name="see-also"></a><span data-ttu-id="256d2-120">Veja também</span><span class="sxs-lookup"><span data-stu-id="256d2-120">See also</span></span>

- <span data-ttu-id="256d2-121">A visão geral do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro) do quantum do kit de desenvolvimento Quantum.</span><span class="sxs-lookup"><span data-stu-id="256d2-121">The Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
- <span data-ttu-id="256d2-122">A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> referência da API.</span><span class="sxs-lookup"><span data-stu-id="256d2-122">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API reference.</span></span>
- <span data-ttu-id="256d2-123">A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> referência da API.</span><span class="sxs-lookup"><span data-stu-id="256d2-123">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API reference.</span></span>
- <span data-ttu-id="256d2-124">A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.DepthCounter> referência da API.</span><span class="sxs-lookup"><span data-stu-id="256d2-124">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.DepthCounter> API reference.</span></span>
