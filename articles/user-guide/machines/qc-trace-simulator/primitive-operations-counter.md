---
title: Contador de operações primitivas – kit de desenvolvimento do Quantum
description: 'Saiba mais sobre o contador de operações do Microsoft QDK Primitive, que usa o simulador de rastreamento do Quantum para rastrear os processos primitivos usados pelas operações em um :::no-loc(Q#)::: programa.'
author: vadym-kl
ms.author: vadym
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.primitive-counter
no-loc:
- ':::no-loc(Q#):::'
- ':::no-loc($$v):::'
ms.openlocfilehash: bf75eb94696a489a587316928bc3f33baa4a1785
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92690947"
---
# <a name="quantum-trace-simulator-primitive-operations-counter"></a><span data-ttu-id="d3bd5-103">Simulador de rastreamento Quantum: contador de operações primitivas</span><span class="sxs-lookup"><span data-stu-id="d3bd5-103">Quantum trace simulator: primitive operations counter</span></span>

<span data-ttu-id="d3bd5-104">O contador de operação primitiva é uma parte do [simulador de rastreamento Quantum](xref:microsoft.quantum.machines.qc-trace-simulator.intro)do kit de desenvolvimento Quantum.</span><span class="sxs-lookup"><span data-stu-id="d3bd5-104">The primitive operation counter is a part of the Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="d3bd5-105">Ele conta o número de processos primitivos usados por cada operação invocada em um programa Quantum.</span><span class="sxs-lookup"><span data-stu-id="d3bd5-105">It counts the number of primitive processes used by every operation invoked in a quantum program.</span></span> 

<span data-ttu-id="d3bd5-106">Todas as <xref:Microsoft.Quantum.Intrinsic> operações são expressas em termos de rotações de qubit único, operações de T, operações de Clifford de qubit único, operações de CNOT e medidas de qubit de vários Pauli observáveis.</span><span class="sxs-lookup"><span data-stu-id="d3bd5-106">All <xref:Microsoft.Quantum.Intrinsic> operations are expressed in terms of single-qubit rotations, T operations, single-qubit Clifford operations, CNOT operations, and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="d3bd5-107">O contador de operações primitivas agrega e coleta estatísticas sobre todas as bordas do [grafo de chamada](https://en.wikipedia.org/wiki/Call_graph)da operação.</span><span class="sxs-lookup"><span data-stu-id="d3bd5-107">The Primitive Operations Counter aggregates and collects statistics over all the edges of the operation's [call graph](https://en.wikipedia.org/wiki/Call_graph).</span></span>

## <a name="invoking-the-primitive-operation-counter"></a><span data-ttu-id="d3bd5-108">Invocando o contador de operação primitiva</span><span class="sxs-lookup"><span data-stu-id="d3bd5-108">Invoking the primitive operation counter</span></span>

<span data-ttu-id="d3bd5-109">Para executar o simulador de rastreamento do Quantum com o contador de operação primitiva, você deve criar uma <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instância, definir a `UsePrimitiveOperationsCounter` propriedade como **true** e, em seguida, criar uma nova <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instância com o `QCTraceSimulatorConfiguration` como o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d3bd5-109">To run the quantum trace simulator with the primitive operation counter, you must create a <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instance, set the `UsePrimitiveOperationsCounter` property to **true** , and then create a new <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instance with the `QCTraceSimulatorConfiguration` as the parameter.</span></span>

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UsePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-primitive-operation-counter-in-a-c-host-program"></a><span data-ttu-id="d3bd5-110">Usando o contador de operação primitiva em um programa de host C#</span><span class="sxs-lookup"><span data-stu-id="d3bd5-110">Using the primitive operation counter in a C# host program</span></span>

<span data-ttu-id="d3bd5-111">O exemplo de C# a seguir nesta seção conta quantas <xref:Microsoft.Quantum.Intrinsic.T> operações são necessárias para implementar a <xref:Microsoft.Quantum.Intrinsic.ccnot> operação, com base no seguinte :::no-loc(Q#)::: código de exemplo:</span><span class="sxs-lookup"><span data-stu-id="d3bd5-111">The C# example that follows in this section counts how many <xref:Microsoft.Quantum.Intrinsic.T> operations are needed to implement the <xref:Microsoft.Quantum.Intrinsic.ccnot> operation, based on the following :::no-loc(Q#)::: sample code:</span></span>

```qsharp
open Microsoft.Quantum.Intrinsic;
operation ApplySampleWithCCNOT() : Unit {

    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

<span data-ttu-id="d3bd5-112">Para verificar se `CCNOT` o requer sete `T` operações e que `ApplySampleWithCCNOT` executa oito `T` operações, use o seguinte código C#:</span><span class="sxs-lookup"><span data-stu-id="d3bd5-112">To check that `CCNOT` requires seven `T` operations and that `ApplySampleWithCCNOT` runs eight `T` operations, use the following C# code:</span></span>

```csharp 
// using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
// using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.UsePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tCountAll = sim.GetMetric<ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
double tCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
```

<span data-ttu-id="d3bd5-113">A primeira parte do programa é executada `ApplySampleWithCCNOT` .</span><span class="sxs-lookup"><span data-stu-id="d3bd5-113">The first part of the program runs `ApplySampleWithCCNOT`.</span></span> <span data-ttu-id="d3bd5-114">A segunda parte usa o [`QCTraceSimulator.GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) método para recuperar o número de `T` operações executadas por `ApplySampleWithCCNOT` :</span><span class="sxs-lookup"><span data-stu-id="d3bd5-114">The second part uses the [`QCTraceSimulator.GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) method to retrieve the number of `T` operations run by `ApplySampleWithCCNOT`:</span></span> 

<span data-ttu-id="d3bd5-115">Quando você chama `GetMetric` com dois parâmetros de tipo, ele retorna o valor da métrica associada a uma determinada borda de gráfico de chamada.</span><span class="sxs-lookup"><span data-stu-id="d3bd5-115">When you call `GetMetric` with two type parameters, it returns the value of the metric associated with a given call graph edge.</span></span> <span data-ttu-id="d3bd5-116">No exemplo anterior, o programa chama a `Primitive.CCNOT` operação dentro `ApplySampleWithCCNOT` e, portanto, o grafo de chamada contém a borda `<Primitive.CCNOT, ApplySampleWithCCNOT>` .</span><span class="sxs-lookup"><span data-stu-id="d3bd5-116">In the preceding example, the program calls the `Primitive.CCNOT` operation  within `ApplySampleWithCCNOT` and therefore the call graph contains the edge `<Primitive.CCNOT, ApplySampleWithCCNOT>`.</span></span> 

<span data-ttu-id="d3bd5-117">Para recuperar o número de `CNOT` operações usadas, adicione a seguinte linha:</span><span class="sxs-lookup"><span data-stu-id="d3bd5-117">To retrieve the number of `CNOT` operations used, add the following line:</span></span>
```csharp
double cxCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.CX);
```

<span data-ttu-id="d3bd5-118">Por fim, você pode gerar todas as estatísticas coletadas pelo contador de operações primitivas no formato CSV usando o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d3bd5-118">Finally, you can output all the statistics collected by the Primitive Operations Counter in CSV format using the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.primitiveOperationsCounter];
```

## <a name="see-also"></a><span data-ttu-id="d3bd5-119">Veja também</span><span class="sxs-lookup"><span data-stu-id="d3bd5-119">See also</span></span>

- <span data-ttu-id="d3bd5-120">A visão geral do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro) do quantum do kit de desenvolvimento Quantum.</span><span class="sxs-lookup"><span data-stu-id="d3bd5-120">The Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
- <span data-ttu-id="d3bd5-121">A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> referência da API.</span><span class="sxs-lookup"><span data-stu-id="d3bd5-121">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API reference.</span></span>
- <span data-ttu-id="d3bd5-122">A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> referência da API.</span><span class="sxs-lookup"><span data-stu-id="d3bd5-122">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API reference.</span></span>
- <span data-ttu-id="d3bd5-123">A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.PrimitiveOperationsGroupsNames> referência da API.</span><span class="sxs-lookup"><span data-stu-id="d3bd5-123">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.PrimitiveOperationsGroupsNames> API reference.</span></span>