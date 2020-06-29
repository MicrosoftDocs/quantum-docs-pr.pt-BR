---
title: Contador de profundidade
description: Saiba mais sobre o contador de profundidade do Microsoft QDK, que reúne as contagens da profundidade de cada operação invocada em um programa Quantum.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.depth-counter
ms.openlocfilehash: 0029a00e6a3563dc542daeda2afa7cabf42441fb
ms.sourcegitcommit: af10179284967bd7a72a52ae7e1c4da65c7d128d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "85415246"
---
# <a name="depth-counter"></a><span data-ttu-id="5a1bb-103">Contador de profundidade</span><span class="sxs-lookup"><span data-stu-id="5a1bb-103">Depth Counter</span></span>

<span data-ttu-id="5a1bb-104">O `Depth Counter` é uma parte do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro)de computador Quantum.</span><span class="sxs-lookup"><span data-stu-id="5a1bb-104">The `Depth Counter` is a part of the quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span>
<span data-ttu-id="5a1bb-105">Ele é usado para reunir contagens que representam o limite inferior da profundidade de cada operação invocada em um programa Quantum.</span><span class="sxs-lookup"><span data-stu-id="5a1bb-105">It is used to gather counts that represent the lower bound of the depth of every operation invoked in a quantum program.</span></span> <span data-ttu-id="5a1bb-106">Todas as operações do <xref:microsoft.quantum.intrinsic> são expressas em termos de rotações qubit únicas, T Gates, Single qubit Clifford Gates, CNOT Gates e medidas de qubit de vários Pauli observáveis.</span><span class="sxs-lookup"><span data-stu-id="5a1bb-106">All operations from <xref:microsoft.quantum.intrinsic> are expressed in terms of single qubit rotations, T gates, single qubit Clifford gates, CNOT gates and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="5a1bb-107">Os usuários podem definir a profundidade para cada uma das operações primitivas por meio do `gateTimes` campo de <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> .</span><span class="sxs-lookup"><span data-stu-id="5a1bb-107">Users can set the depth for each of the primitive operations via the `gateTimes` field of <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>.</span></span>

<span data-ttu-id="5a1bb-108">Por padrão, todas as operações têm profundidade 0, exceto o portão T que tem profundidade 1.</span><span class="sxs-lookup"><span data-stu-id="5a1bb-108">By default, all operations have depth 0 except the T gate which has depth 1.</span></span> <span data-ttu-id="5a1bb-109">Isso significa que, por padrão, somente a profundidade de operações T é calculada (o que geralmente é desejável).</span><span class="sxs-lookup"><span data-stu-id="5a1bb-109">This means that by default, only the T depth of operations is computed (which is often desirable).</span></span> <span data-ttu-id="5a1bb-110">As estatísticas coletadas são agregadas em todas as bordas do grafo de chamada de operações.</span><span class="sxs-lookup"><span data-stu-id="5a1bb-110">Collected statistics are aggregated over all the edges of the operations call graph.</span></span> 

<span data-ttu-id="5a1bb-111">Agora, vamos calcular a <xref:microsoft.quantum.intrinsic.t> profundidade da <xref:microsoft.quantum.intrinsic.ccnot> operação.</span><span class="sxs-lookup"><span data-stu-id="5a1bb-111">Let us now compute the <xref:microsoft.quantum.intrinsic.t> depth of the <xref:microsoft.quantum.intrinsic.ccnot> operation.</span></span> <span data-ttu-id="5a1bb-112">Usaremos o seguinte código de exemplo de Q #:</span><span class="sxs-lookup"><span data-stu-id="5a1bb-112">We will use the following Q# sample code:</span></span>

```qsharp
open Microsoft.Quantum.Intrinsic;

operation ApplySampleWithCCNOT() : Unit {
    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

## <a name="using-depth-counter-within-a-c-program"></a><span data-ttu-id="5a1bb-113">Usando o contador de profundidade em um programa em C#</span><span class="sxs-lookup"><span data-stu-id="5a1bb-113">Using Depth Counter within a C# Program</span></span>

<span data-ttu-id="5a1bb-114">Para verificar se `CCNOT` `T` o tem profundidade 5 e `ApplySampleWithCCNOT` tem `T` profundidade 6, podemos usar o seguinte código C#:</span><span class="sxs-lookup"><span data-stu-id="5a1bb-114">To check that `CCNOT` has `T` depth 5 and `ApplySampleWithCCNOT` has `T` depth 6 we can use the following C# code:</span></span>

```csharp
using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.useDepthCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tDepth = sim.GetMetric<Intrinsic.CCNOT, ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
```

<span data-ttu-id="5a1bb-115">A primeira parte do programa é executada `ApplySampleWithCCNOT` .</span><span class="sxs-lookup"><span data-stu-id="5a1bb-115">The first part of the program executes `ApplySampleWithCCNOT`.</span></span> <span data-ttu-id="5a1bb-116">Na segunda parte, usamos o método `QCTraceSimulator.GetMetric` para obter a `T` profundidade de `CCNOT` e `ApplySampleWithCCNOT` :</span><span class="sxs-lookup"><span data-stu-id="5a1bb-116">In the second part, we use the method `QCTraceSimulator.GetMetric` to get the `T` depth of `CCNOT` and `ApplySampleWithCCNOT`:</span></span> 

```csharp
double tDepth = sim.GetMetric<Intrinsic.CCNOT, ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
```

<span data-ttu-id="5a1bb-117">Por fim, para gerar todas as estatísticas coletadas pelo `Depth Counter` no formato CSV, podemos usar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5a1bb-117">Finally, to output all the statistics collected by `Depth Counter` in CSV format we can use the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.depthCounter];
```

## <a name="see-also"></a><span data-ttu-id="5a1bb-118">Veja também</span><span class="sxs-lookup"><span data-stu-id="5a1bb-118">See also</span></span> ##

- <span data-ttu-id="5a1bb-119">A visão geral do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro) do computador Quantum.</span><span class="sxs-lookup"><span data-stu-id="5a1bb-119">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
