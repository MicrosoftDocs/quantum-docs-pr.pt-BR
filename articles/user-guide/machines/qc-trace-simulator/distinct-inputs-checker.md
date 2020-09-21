---
title: Verificador de entradas distintos – kit de desenvolvimento Quantum
description: Saiba mais sobre o verificador de entradas distintos da Microsoft QDK, que usa o simulador de rastreamento do Quantum para verificar o Q# código em busca de possíveis conflitos com o qubits compartilhado.
author: vadym-kl
ms.author: vadym
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.distinct-inputs
no-loc:
- Q#
- $$v
ms.openlocfilehash: bcb0bc92a546279496d27ad9b8c5f943ac133e2a
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90833460"
---
# <a name="quantum-trace-simulator-distinct-inputs-checker"></a><span data-ttu-id="fed8d-103">Simulador de rastreamento Quantum: verificador de entradas distintos</span><span class="sxs-lookup"><span data-stu-id="fed8d-103">Quantum trace simulator: distinct inputs checker</span></span>

<span data-ttu-id="fed8d-104">O verificador de entradas distintos faz parte do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro)Quantum do kit de desenvolvimento Quantum.</span><span class="sxs-lookup"><span data-stu-id="fed8d-104">The distinct inputs checker is a part of the Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="fed8d-105">Você pode usá-lo para detectar possíveis bugs no código causado por conflitos com qubits compartilhados.</span><span class="sxs-lookup"><span data-stu-id="fed8d-105">You can use it to detect potential bugs in the code caused by conflicts with shared qubits.</span></span> 

## <a name="conflicts-with-shared-qubits"></a><span data-ttu-id="fed8d-106">Conflitos com qubits compartilhados</span><span class="sxs-lookup"><span data-stu-id="fed8d-106">Conflicts with shared qubits</span></span>

<span data-ttu-id="fed8d-107">Considere o seguinte trecho de Q# código para ilustrar os problemas detectados pelo verificador de entradas distintos:</span><span class="sxs-lookup"><span data-stu-id="fed8d-107">Consider the following piece of Q# code to illustrate the issues detected by the distinct inputs checker:</span></span>

```qsharp
operation ApplyBoth(
    q1 : Qubit,
    q2 : Qubit,
    op1 : (Qubit => Unit),
    op2 : (Qubit => Unit))
: Unit {
    op1(q1);
    op2(q2);
}
```

<span data-ttu-id="fed8d-108">Ao examinar esse programa, você pode assumir que a ordem em que ele chama e não `op1` `op2` importa, porque `q1` e `q2` são diferentes qubits e operações que atuam em diferentes qubits.</span><span class="sxs-lookup"><span data-stu-id="fed8d-108">When you look at this program, you can assume that the order in which it calls `op1` and `op2` does not matter, because `q1` and `q2` are different qubits and operations acting on different qubits commute.</span></span> 

<span data-ttu-id="fed8d-109">Agora, considere este exemplo:</span><span class="sxs-lookup"><span data-stu-id="fed8d-109">Now, consider this example:</span></span>

```qsharp
operation ApplyWithNonDistinctInputs() : Unit {
    using (qubits = Qubit[3]) {
        let op1 = CNOT(_, qubits[1]);
        let op2 = CNOT(qubits[1], _);
        ApplyBoth(qubits[0], qubits[2], op1, op2);
    }
}
```

<span data-ttu-id="fed8d-110">Observe que `op1` e `op2` são obtidos usando o aplicativo parcial e compartilham um qubit.</span><span class="sxs-lookup"><span data-stu-id="fed8d-110">Note that `op1` and `op2` are both obtained using partial application and share a qubit.</span></span> <span data-ttu-id="fed8d-111">Quando você chama `ApplyBoth` neste exemplo, o resultado da operação depende da ordem de `op1` e `op2` dentro `ApplyBoth` , não é o que você esperaria acontecer.</span><span class="sxs-lookup"><span data-stu-id="fed8d-111">When you call `ApplyBoth` in this example, the result of the operation depends on the order of `op1` and `op2` inside `ApplyBoth` - not what you would expect to happen.</span></span> <span data-ttu-id="fed8d-112">Quando você habilita o verificador de entradas distintos, ele detecta essas situações e gera um `DistinctInputsCheckerException` .</span><span class="sxs-lookup"><span data-stu-id="fed8d-112">When you enable the distinct inputs checker, it detects such situations and throws a `DistinctInputsCheckerException`.</span></span> <span data-ttu-id="fed8d-113">Para obter mais informações, consulte <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException> na Q# biblioteca de API.</span><span class="sxs-lookup"><span data-stu-id="fed8d-113">For more information, see <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException> in the Q# API library.</span></span>

## <a name="invoking-the-distinct-inputs-checker"></a><span data-ttu-id="fed8d-114">Invocando o verificador de entradas distintos</span><span class="sxs-lookup"><span data-stu-id="fed8d-114">Invoking the distinct inputs checker</span></span>

<span data-ttu-id="fed8d-115">Para executar o simulador de rastreamento do Quantum com o verificador de entradas distintos, você deve criar uma <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instância, definir a `UseDistinctInputsChecker` propriedade como **true**e, em seguida, criar uma nova <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instância com `QCTraceSimulatorConfiguration` como o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="fed8d-115">To run the quantum trace simulator with the distinct inputs checker you must create a <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instance, set the `UseDistinctInputsChecker` property to **true**, and then create a new <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instance with `QCTraceSimulatorConfiguration` as the parameter.</span></span> 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseDistinctInputsChecker = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-distinct-inputs-checker-in-a-c-host-program"></a><span data-ttu-id="fed8d-116">Usando o verificador de entradas distintos em um programa de host C#</span><span class="sxs-lookup"><span data-stu-id="fed8d-116">Using the distinct inputs checker in a C# host program</span></span>

<span data-ttu-id="fed8d-117">Veja a seguir um exemplo de programa de host C# que usa o simulador de rastreamento Quantum com o verificador de entradas distintos habilitado:</span><span class="sxs-lookup"><span data-stu-id="fed8d-117">The following is an example of C# host program that uses the quantum trace simulator with the distinct inputs checker enabled:</span></span>

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
            var traceSimCfg = new QCTraceSimulatorConfiguration();
            traceSimCfg.UseDistinctInputsChecker = true; //enables distinct inputs checker
            QCTraceSimulator sim = new QCTraceSimulator(traceSimCfg);
            var res = MyQuantumProgram.Run().Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="fed8d-118">Consulte também</span><span class="sxs-lookup"><span data-stu-id="fed8d-118">See also</span></span>

- <span data-ttu-id="fed8d-119">A visão geral do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro) do quantum do kit de desenvolvimento Quantum.</span><span class="sxs-lookup"><span data-stu-id="fed8d-119">The Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
- <span data-ttu-id="fed8d-120">A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> referência da API.</span><span class="sxs-lookup"><span data-stu-id="fed8d-120">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API reference.</span></span>
- <span data-ttu-id="fed8d-121">A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> referência da API.</span><span class="sxs-lookup"><span data-stu-id="fed8d-121">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API reference.</span></span>
- <span data-ttu-id="fed8d-122">A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException> referência da API.</span><span class="sxs-lookup"><span data-stu-id="fed8d-122">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException> API reference.</span></span>
