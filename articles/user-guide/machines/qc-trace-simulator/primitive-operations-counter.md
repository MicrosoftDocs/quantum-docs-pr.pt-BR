---
title: Contador de operações primitivas
description: Saiba mais sobre o contador de operações do Microsoft QDK Primitive, que controla o número de execuções primitivas usadas pelas operações em um programa Quantum.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.primitive-counter
ms.openlocfilehash: 8bdb0aed370e72b58b23025f1685ad7ce1a77a43
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274257"
---
# <a name="primitive-operations-counter"></a><span data-ttu-id="06259-103">Contador de operações primitivas</span><span class="sxs-lookup"><span data-stu-id="06259-103">Primitive Operations Counter</span></span>  

<span data-ttu-id="06259-104">O `Primitive Operations Counter` é uma parte do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro)de computador Quantum.</span><span class="sxs-lookup"><span data-stu-id="06259-104">The `Primitive Operations Counter` is a part of the quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="06259-105">Ele conta o número de execuções primitivas usadas por cada operação invocada em um programa Quantum.</span><span class="sxs-lookup"><span data-stu-id="06259-105">It counts the number of primitive executions used by every operation invoked in a quantum program.</span></span> <span data-ttu-id="06259-106">Todas as operações do `Microsoft.Quantum.Intrinsic` são expressas em termos de rotações qubit únicas, T Gates, Single qubit Clifford Gates, CNOT Gates e medidas de qubit de vários Pauli observáveis.</span><span class="sxs-lookup"><span data-stu-id="06259-106">All operations from `Microsoft.Quantum.Intrinsic` are expressed in terms of single qubit rotations, T gates, single qubit Clifford gates, CNOT gates and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="06259-107">As estatísticas coletadas são agregadas nas bordas do grafo de chamada de operações.</span><span class="sxs-lookup"><span data-stu-id="06259-107">Collected statistics are aggregated over the edges of the operations call graph.</span></span> <span data-ttu-id="06259-108">Agora, vamos contar quantas `T` Gates são necessárias para implementar a `CCNOT` operação.</span><span class="sxs-lookup"><span data-stu-id="06259-108">Let us now count how many `T` gates are needed to implement the `CCNOT` operation.</span></span> 

```qsharp
open Microsoft.Quantum.Intrinsic;
operation ApplySampleWithCCNOT() : Unit {

    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    } 
}
```

## <a name="using-the-primitive-operations-counter-within-a-c-program"></a><span data-ttu-id="06259-109">Usando o contador de operações primitivas em um programa C#</span><span class="sxs-lookup"><span data-stu-id="06259-109">Using the Primitive Operations Counter within a C# Program</span></span>

<span data-ttu-id="06259-110">Para verificar se `CCNOT` realmente requer 7 `T` Gates e que `ApplySampleWithCCNOT` Execute 8 `T` Gates, podemos usar o seguinte código C#:</span><span class="sxs-lookup"><span data-stu-id="06259-110">To check that `CCNOT` indeed requires 7 `T` gates and that `ApplySampleWithCCNOT` executes 8 `T` gates we can use the following C# code:</span></span>

```csharp 
// using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
// using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.usePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tCountAll = sim.GetMetric<ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
double tCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
```

<span data-ttu-id="06259-111">A primeira parte do programa é executada `ApplySampleWithCCNOT` .</span><span class="sxs-lookup"><span data-stu-id="06259-111">The first part of the program executes `ApplySampleWithCCNOT`.</span></span> <span data-ttu-id="06259-112">Na segunda parte, usamos o método `QCTraceSimulator.GetMetric` para obter o número de T Gates executadas por `ApplySampleWithCCNOT` :</span><span class="sxs-lookup"><span data-stu-id="06259-112">In the second part, we use the method `QCTraceSimulator.GetMetric` to get the number of T gates executed by `ApplySampleWithCCNOT`:</span></span> 

```csharp
double tCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
double tCountAll = sim.GetMetric<ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
```

<span data-ttu-id="06259-113">Quando `GetMetric` é chamado com dois parâmetros de tipo, ele retorna o valor da métrica associada a uma determinada borda de gráfico de chamada.</span><span class="sxs-lookup"><span data-stu-id="06259-113">When `GetMetric` is called with two type parameters it returns the value of the metric associated with a given call graph edge.</span></span> <span data-ttu-id="06259-114">Em nossa operação de exemplo `Primitive.CCNOT` é chamada dentro `ApplySampleWithCCNOT` e, portanto, o grafo de chamada contém a borda `<Primitive.CCNOT, ApplySampleWithCCNOT>` .</span><span class="sxs-lookup"><span data-stu-id="06259-114">In our example operation `Primitive.CCNOT` is called within `ApplySampleWithCCNOT` and therefore the call graph contains the edge `<Primitive.CCNOT, ApplySampleWithCCNOT>`.</span></span> 

<span data-ttu-id="06259-115">Para obter o número de `CNOT` Gates usadas, podemos adicionar a seguinte linha:</span><span class="sxs-lookup"><span data-stu-id="06259-115">To get the number of `CNOT` gates used, we can add the following line:</span></span>
```csharp
double cxCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.CX);
```

<span data-ttu-id="06259-116">Por fim, para gerar todas as estatísticas coletadas pelo contador portão no formato CSV, podemos usar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="06259-116">Finally, to output all the statistics collected by the gate counter in CSV format we can use the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.primitiveOperationsCounter];
```

## <a name="see-also"></a><span data-ttu-id="06259-117">Veja também</span><span class="sxs-lookup"><span data-stu-id="06259-117">See also</span></span> ##

- <span data-ttu-id="06259-118">A visão geral do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro) do computador Quantum.</span><span class="sxs-lookup"><span data-stu-id="06259-118">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
