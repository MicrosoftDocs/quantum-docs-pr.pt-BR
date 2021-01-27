---
title: Contador de largura – kit de desenvolvimento do Quantum
description: Saiba mais sobre o contador de largura QDK da Microsoft, que usa o simulador de rastreamento Quantum para contar o número de qubits alocados e emprestados por operações em um Q# programa.
author: vadym-kl
ms.author: vadym
ms.date: 06/25/2020
ms.topic: conceptual
uid: microsoft.quantum.machines.qc-trace-simulator.width-counter
no-loc:
- Q#
- $$v
ms.openlocfilehash: e9a526ee1440544aace922bd83c6ea39cb83c1ae
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858589"
---
# <a name="quantum-trace-simulator-width-counter"></a><span data-ttu-id="a30f5-103">Simulador de rastreamento Quantum: contador de largura</span><span class="sxs-lookup"><span data-stu-id="a30f5-103">Quantum trace simulator: width counter</span></span>

<span data-ttu-id="a30f5-104">O contador de largura faz parte do [simulador de rastreamento Quantum](xref:microsoft.quantum.machines.qc-trace-simulator.intro)do kit de desenvolvimento Quantum.</span><span class="sxs-lookup"><span data-stu-id="a30f5-104">The width counter is a part of the Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="a30f5-105">Você pode usá-lo para contar o número de qubits alocadas e emprestadas por cada operação em um Q# programa.</span><span class="sxs-lookup"><span data-stu-id="a30f5-105">You can use it to count the number of qubits allocated and borrowed by each operation in a Q# program.</span></span> <span data-ttu-id="a30f5-106">Algumas operações primitivas podem alocar qubits extras, por exemplo, operações controladas multiplicadas `X` ou operações controladas `T` .</span><span class="sxs-lookup"><span data-stu-id="a30f5-106">Some primitive operations can allocate extra qubits, for example, multiply controlled `X` operations or controlled `T` operations.</span></span>

## <a name="invoking-the-width-counter"></a><span data-ttu-id="a30f5-107">Invocando o contador de largura</span><span class="sxs-lookup"><span data-stu-id="a30f5-107">Invoking the width counter</span></span>

<span data-ttu-id="a30f5-108">Para executar o simulador de rastreamento do Quantum com o contador de largura, você deve criar uma <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instância, definir a `UseWidthCounter` propriedade como **true** e, em seguida, criar uma nova <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instância com o `QCTraceSimulatorConfiguration` como o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a30f5-108">To run the quantum trace simulator with the width counter, you must create a <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instance, set the `UseWidthCounter` property to **true**, and then create a new <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instance with the `QCTraceSimulatorConfiguration` as the parameter.</span></span> 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseWidthCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-width-counter-in-a-c-host-program"></a><span data-ttu-id="a30f5-109">Usando o contador de largura em um programa de host C#</span><span class="sxs-lookup"><span data-stu-id="a30f5-109">Using the width counter in a C# host program</span></span>

<span data-ttu-id="a30f5-110">O exemplo de C# a seguir nesta seção computa o número de qubits extras alocados pela implementação de uma operação controlada de multiplicação <xref:Microsoft.Quantum.Intrinsic.X> , com base no seguinte Q# código de exemplo:</span><span class="sxs-lookup"><span data-stu-id="a30f5-110">The C# example that follows in this section computes the number of extra qubits allocated by the implementation of a multiply controlled <xref:Microsoft.Quantum.Intrinsic.X> operation, based on the following Q# sample code:</span></span>

```qsharp
open Microsoft.Quantum.Intrinsic;
open Microsoft.Quantum.Arrays;
operation ApplyMultiControlledX( numberOfQubits : Int ) : Unit {
    using(qubits = Qubit[numberOfQubits]) {
        Controlled X (Rest(qubits), Head(qubits));
    } 
}
```

<span data-ttu-id="a30f5-111">A operação de multiplicação controlada <xref:Microsoft.Quantum.Intrinsic.X> atua em um total de cinco qubits, aloca dois [qubits auxiliares](xref:microsoft.quantum.glossary#ancilla)e tem uma largura de entrada de **5**.</span><span class="sxs-lookup"><span data-stu-id="a30f5-111">The multiply controlled <xref:Microsoft.Quantum.Intrinsic.X> operation acts on a total of five qubits, allocates two [ancillary qubits](xref:microsoft.quantum.glossary#ancilla), and has an input width of **5**.</span></span> <span data-ttu-id="a30f5-112">Use o seguinte programa C# para verificar as contagens:</span><span class="sxs-lookup"><span data-stu-id="a30f5-112">Use the following C# program to verify the counts:</span></span>

```csharp 
var config = new QCTraceSimulatorConfiguration();
config.UseWidthCounter = true;
var sim = new QCTraceSimulator(config);
int totalNumberOfQubits = 5;
var res = ApplyMultiControlledX.Run(sim, totalNumberOfQubits).Result;

double allocatedQubits = 
    sim.GetMetric<Primitive.X, ApplyMultiControlledX>(
        WidthCounter.Metrics.ExtraWidth,
        functor: OperationFunctor.Controlled); 

double inputWidth =
    sim.GetMetric<Primitive.X, ApplyMultiControlledX>(
        WidthCounter.Metrics.InputWidth,
        functor: OperationFunctor.Controlled);
```

<span data-ttu-id="a30f5-113">A primeira parte do programa executa a `ApplyMultiControlledX` operação.</span><span class="sxs-lookup"><span data-stu-id="a30f5-113">The first part of the program runs the `ApplyMultiControlledX` operation.</span></span> <span data-ttu-id="a30f5-114">A segunda parte usa o [`QCTraceSimulator.GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) método para recuperar o número de qubits alocadas, bem como o número de qubits que a `Controlled X` operação recebeu como entrada.</span><span class="sxs-lookup"><span data-stu-id="a30f5-114">The second part uses the [`QCTraceSimulator.GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) method to retrieve the number of allocated qubits as well as the number of qubits that the `Controlled X` operation received as input.</span></span> 

<span data-ttu-id="a30f5-115">Por fim, você pode gerar todas as estatísticas coletadas pelo contador de largura no formato CSV usando o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a30f5-115">Finally, you can output all the statistics collected by the width counter in CSV format using the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.widthCounter];
```

## <a name="see-also"></a><span data-ttu-id="a30f5-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="a30f5-116">See also</span></span>

- <span data-ttu-id="a30f5-117">A visão geral do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro) do quantum do kit de desenvolvimento Quantum.</span><span class="sxs-lookup"><span data-stu-id="a30f5-117">The Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
- <span data-ttu-id="a30f5-118">A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> referência da API.</span><span class="sxs-lookup"><span data-stu-id="a30f5-118">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API reference.</span></span>
- <span data-ttu-id="a30f5-119">A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> referência da API.</span><span class="sxs-lookup"><span data-stu-id="a30f5-119">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API reference.</span></span>
- <span data-ttu-id="a30f5-120">A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.WidthCounter> referência da API.</span><span class="sxs-lookup"><span data-stu-id="a30f5-120">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.WidthCounter> API reference.</span></span>
