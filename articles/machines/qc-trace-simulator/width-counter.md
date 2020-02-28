---
title: Contador de largura
description: Saiba mais sobre o contador de largura QDK da Microsoft, que conta o número de qubits alocadas e emprestadas por cada operação em um programa Quantum.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.width-counter
ms.openlocfilehash: a76292222950310acc90dded02980e4a5b792e76
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907079"
---
# <a name="width-counter"></a><span data-ttu-id="e91f3-103">Contador de largura</span><span class="sxs-lookup"><span data-stu-id="e91f3-103">Width Counter</span></span>

<span data-ttu-id="e91f3-104">O `Width Counter` conta o número de qubits alocados e emprestados por cada operação.</span><span class="sxs-lookup"><span data-stu-id="e91f3-104">The `Width Counter` counts the number of qubits allocated and borrowed by each operation.</span></span>
<span data-ttu-id="e91f3-105">Todas as operações do namespace `Microsoft.Quantum.Intrinsic` são expressas em termos de rotações qubit únicas, T Gates, Single qubit Clifford Gates, CNOT Gates e medidas de qubit de vários Pauli observáveis.</span><span class="sxs-lookup"><span data-stu-id="e91f3-105">All operations from the `Microsoft.Quantum.Intrinsic` namespace are expressed in terms of single qubit rotations, T gates, single qubit Clifford gates, CNOT gates and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="e91f3-106">Algumas das operações primitivas podem alocar qubits extras.</span><span class="sxs-lookup"><span data-stu-id="e91f3-106">Some of the primitive operations can allocate extra qubits.</span></span> <span data-ttu-id="e91f3-107">Por exemplo, multiplique `X` Gates controlado ou Gates de `T` controlado.</span><span class="sxs-lookup"><span data-stu-id="e91f3-107">For example, multiply controlled `X` gates or controlled `T` gates.</span></span> <span data-ttu-id="e91f3-108">Vamos calcular o número de qubits extras alocados pela implementação de um portão de `X` controlado por multiplicação:</span><span class="sxs-lookup"><span data-stu-id="e91f3-108">Let us compute the number of extra qubits allocated by the implementation of a multiply controlled `X` gate:</span></span>

```qsharp
open Microsoft.Quantum.Intrinsic;
open Microsoft.Quantum.Arrays;
operation ApplyMultiControlledX( numberOfQubits : Int ) : Unit {
    using(qubits = Qubit[numberOfQubits]) {
        Controlled X (Rest(qubits), Head(qubits));
    } 
}
```

## <a name="using-width-counter-within-a-c-program"></a><span data-ttu-id="e91f3-109">Usando o contador de largura C# dentro de um programa</span><span class="sxs-lookup"><span data-stu-id="e91f3-109">Using Width Counter within a C# Program</span></span>

<span data-ttu-id="e91f3-110">Multiplicar `X` controlado atuando em um total de 5 qubits alocará 2 qubits auxiliares e sua largura de entrada será 5.</span><span class="sxs-lookup"><span data-stu-id="e91f3-110">Multiply controlled `X` acting on a total of 5 qubits will allocate 2 ancillary qubits and its input width will be 5.</span></span> <span data-ttu-id="e91f3-111">Para verificar se esse é o caso, podemos usar o seguinte C# programa:</span><span class="sxs-lookup"><span data-stu-id="e91f3-111">To check that this is the case, we can use the following C# program:</span></span>

```csharp 
var config = new QCTraceSimulatorConfiguration();
config.useWidthCounter = true;
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

<span data-ttu-id="e91f3-112">A primeira parte do programa executa `ApplyMultiControlledX`.</span><span class="sxs-lookup"><span data-stu-id="e91f3-112">The first part of the program executes `ApplyMultiControlledX`.</span></span> <span data-ttu-id="e91f3-113">Na segunda parte, usamos o método `QCTraceSimulator.GetMetric` para obter o número de qubits alocadas, bem como o número de qubits que controlavam `X` recebido como entrada.</span><span class="sxs-lookup"><span data-stu-id="e91f3-113">In the second part we use the method `QCTraceSimulator.GetMetric` to get the number of allocated qubits as well as the number of qubits that Controlled `X` received as input.</span></span> 

<span data-ttu-id="e91f3-114">Por fim, para gerar todas as estatísticas coletadas pelo contador de largura no formato CSV, podemos usar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e91f3-114">Finally, to output all the statistics collected by width counter in CSV format we can use the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.widthCounter];
```

## <a name="see-also"></a><span data-ttu-id="e91f3-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e91f3-115">See also</span></span> ##

- <span data-ttu-id="e91f3-116">A visão geral do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro) do computador Quantum.</span><span class="sxs-lookup"><span data-stu-id="e91f3-116">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
