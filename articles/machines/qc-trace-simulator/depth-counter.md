---
title: Contador de profundidade | Simulador de rastreamento de computador Quantum | Microsoft Docs
description: Visão geral do simulador de rastreamento de computador quântico
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.depth-counter
ms.openlocfilehash: 07f927c794e2c62e53e4e053b5bc683d24bbed8d
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820463"
---
# <a name="depth-counter"></a><span data-ttu-id="609bc-103">Contador de profundidade</span><span class="sxs-lookup"><span data-stu-id="609bc-103">Depth Counter</span></span>

<span data-ttu-id="609bc-104">O `Depth Counter` é uma parte do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro)de computador Quantum.</span><span class="sxs-lookup"><span data-stu-id="609bc-104">The `Depth Counter` is a part of the quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span>
<span data-ttu-id="609bc-105">Ele é usado para reunir contagens da profundidade de cada operação invocada em um programa Quantum.</span><span class="sxs-lookup"><span data-stu-id="609bc-105">It is used to gather counts of the depth of every operation invoked in a quantum program.</span></span> <span data-ttu-id="609bc-106">Todas as operações de <xref:microsoft.quantum.intrinsic> são expressas em termos de rotações qubit únicas, T Gates, Single qubit Clifford Gates, CNOT Gates e medidas de qubit de vários Pauli observáveis.</span><span class="sxs-lookup"><span data-stu-id="609bc-106">All operations from <xref:microsoft.quantum.intrinsic> are expressed in terms of single qubit rotations, T gates, single qubit Clifford gates, CNOT gates and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="609bc-107">Os usuários podem definir a profundidade para cada uma das operações primitivas por meio do campo `gateTimes` de <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>.</span><span class="sxs-lookup"><span data-stu-id="609bc-107">Users can set the depth for each of the primitive operations via the `gateTimes` field of <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>.</span></span>

<span data-ttu-id="609bc-108">Por padrão, todas as operações têm profundidade 0, exceto o portão T que tem profundidade 1.</span><span class="sxs-lookup"><span data-stu-id="609bc-108">By default, all operations have depth 0 except the T gate which has depth 1.</span></span> <span data-ttu-id="609bc-109">Isso significa que, por padrão, somente a profundidade de operações T é calculada (o que geralmente é desejável).</span><span class="sxs-lookup"><span data-stu-id="609bc-109">This means that by default, only the T depth of operations is computed (which is often desirable).</span></span> <span data-ttu-id="609bc-110">As estatísticas coletadas são agregadas em todas as bordas do grafo de chamada de operações.</span><span class="sxs-lookup"><span data-stu-id="609bc-110">Collected statistics are aggregated over all the edges of the operations call graph.</span></span> 

<span data-ttu-id="609bc-111">Agora, vamos calcular a profundidade de <xref:microsoft.quantum.intrinsic.t> da operação <xref:microsoft.quantum.intrinsic.ccnot>.</span><span class="sxs-lookup"><span data-stu-id="609bc-111">Let us now compute the <xref:microsoft.quantum.intrinsic.t> depth of the <xref:microsoft.quantum.intrinsic.ccnot> operation.</span></span> <span data-ttu-id="609bc-112">Usaremos o seguinte código de exemplo de Q #:</span><span class="sxs-lookup"><span data-stu-id="609bc-112">We will use the following Q# sample code:</span></span>

```qsharp
open Microsoft.Quantum.Intrinsic;

operation ApplySampleWithCCNOT() : Unit {
    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

## <a name="using-depth-counter-within-a-c-program"></a><span data-ttu-id="609bc-113">Usando o contador de profundidade C# em um programa</span><span class="sxs-lookup"><span data-stu-id="609bc-113">Using Depth Counter within a C# Program</span></span>

<span data-ttu-id="609bc-114">Para verificar se `CCNOT` tem `T` profundidade 5 e `ApplySampleWithCCNOT` tem `T` profundidade 6, podemos usar o seguinte C# código:</span><span class="sxs-lookup"><span data-stu-id="609bc-114">To check that `CCNOT` has `T` depth 5 and `ApplySampleWithCCNOT` has `T` depth 6 we can use the following C# code:</span></span>

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

<span data-ttu-id="609bc-115">A primeira parte do programa executa `ApplySampleWithCCNOT`.</span><span class="sxs-lookup"><span data-stu-id="609bc-115">The first part of the program executes `ApplySampleWithCCNOT`.</span></span> <span data-ttu-id="609bc-116">Na segunda parte, usamos o método `QCTraceSimulator.GetMetric` para obter a profundidade de `T` de `CCNOT` e `ApplySampleWithCCNOT`:</span><span class="sxs-lookup"><span data-stu-id="609bc-116">In the second part, we use the method `QCTraceSimulator.GetMetric` to get the `T` depth of `CCNOT` and `ApplySampleWithCCNOT`:</span></span> 

```csharp
double tDepth = sim.GetMetric<Intrinsic.CCNOT, ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
```

<span data-ttu-id="609bc-117">Por fim, para gerar todas as estatísticas coletadas por `Depth Counter` no formato CSV, podemos usar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="609bc-117">Finally, to output all the statistics collected by `Depth Counter` in CSV format we can use the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.depthCounter];
```

## <a name="see-also"></a><span data-ttu-id="609bc-118">Consulte também</span><span class="sxs-lookup"><span data-stu-id="609bc-118">See also</span></span> ##

- <span data-ttu-id="609bc-119">A visão geral do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro) do computador Quantum.</span><span class="sxs-lookup"><span data-stu-id="609bc-119">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
