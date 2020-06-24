---
title: Verificador de entradas distintos
description: 'Saiba mais sobre o verificador de entradas distintos da Microsoft QDK, que verifica o código de Q # em busca de possíveis conflitos com o qubits compartilhado.'
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.distinct-inputs
ms.openlocfilehash: 11a0573242c8afb12f242aa3be5f9cff18290452
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274265"
---
# <a name="distinct-inputs-checker"></a><span data-ttu-id="e1217-103">Verificador de entradas distintos</span><span class="sxs-lookup"><span data-stu-id="e1217-103">Distinct Inputs Checker</span></span>

<span data-ttu-id="e1217-104">O `Distinct Inputs Checker` é uma parte do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro)de computador Quantum.</span><span class="sxs-lookup"><span data-stu-id="e1217-104">The `Distinct Inputs Checker` is a part of the quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="e1217-105">Ele foi projetado para detectar possíveis bugs no código.</span><span class="sxs-lookup"><span data-stu-id="e1217-105">It is designed for detecting potential bugs in the code.</span></span> <span data-ttu-id="e1217-106">Considere a seguinte parte do código do Q # para ilustrar os problemas detectados por este pacote:</span><span class="sxs-lookup"><span data-stu-id="e1217-106">Consider the following piece of Q# code to illustrate the issues detected by this package:</span></span>

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

<span data-ttu-id="e1217-107">Quando o usuário examina esse programa, ele pressupõe que a ordem na qual `op1` e `op2` são chamados não importa porque `q1` e `q2` são qubits diferentes e operações que atuam em qubits diferentes.</span><span class="sxs-lookup"><span data-stu-id="e1217-107">When the user looks at this program, they assume that the order in which `op1` and `op2` are called does not matter because `q1` and `q2` are different qubits and operations acting on different qubits commute.</span></span> <span data-ttu-id="e1217-108">Agora, vamos considerar um exemplo, em que esta operação é usada:</span><span class="sxs-lookup"><span data-stu-id="e1217-108">Let us now consider an example, where this operation is used:</span></span>

```qsharp
operation ApplyWithNonDistinctInputs() : Unit {
    using (qubits = Qubit[3]) {
        let op1 = CNOT(_, qubits[1]);
        let op2 = CNOT(qubits[1], _);
        ApplyBoth(qubits[0], qubits[2], op1, op2);
    }
}
```

<span data-ttu-id="e1217-109">Agora `op1` , `op2` ambos são obtidos usando o aplicativo parcial e compartilham um qubit.</span><span class="sxs-lookup"><span data-stu-id="e1217-109">Now `op1` and `op2` are both obtained using partial application and share a qubit.</span></span> <span data-ttu-id="e1217-110">Quando o usuário chama `ApplyBoth` no exemplo acima, o resultado da operação dependerá da ordem de `op1` e `op2` dentro `ApplyBoth` .</span><span class="sxs-lookup"><span data-stu-id="e1217-110">When the user calls `ApplyBoth` in the example above the result of the operation will depend on the order of `op1` and `op2` inside `ApplyBoth`.</span></span> <span data-ttu-id="e1217-111">Isso definitivamente não é o que o usuário esperaria acontecer.</span><span class="sxs-lookup"><span data-stu-id="e1217-111">This is definitely not what the user would expect to happen.</span></span> <span data-ttu-id="e1217-112">O `Distinct Inputs Checker` detectará essas situações quando for habilitado e gerará `DistinctInputsCheckerException` .</span><span class="sxs-lookup"><span data-stu-id="e1217-112">The `Distinct Inputs Checker` will detect such situations when enabled and will throw `DistinctInputsCheckerException`.</span></span> <span data-ttu-id="e1217-113">Consulte a documentação da API em [DistinctInputsCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="e1217-113">See the API documentation on [DistinctInputsCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException) for more details.</span></span>

## <a name="using-the-distinct-inputs-checker-in-your-c-program"></a><span data-ttu-id="e1217-114">Usando o verificador de entradas distintos em seu programa C#</span><span class="sxs-lookup"><span data-stu-id="e1217-114">Using the Distinct Inputs Checker in your C# Program</span></span>

<span data-ttu-id="e1217-115">Veja a seguir um exemplo de código de driver C# para usar o simulador de rastreamento de computador Quantum com o `Distinct Inputs Checker` habilitado:</span><span class="sxs-lookup"><span data-stu-id="e1217-115">The following is an example of C# driver code for using the quantum computer trace simulator with the `Distinct Inputs Checker` enabled:</span></span>

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
            traceSimCfg.useDistinctInputsChecker = true; //enables distinct inputs checker
            QCTraceSimulator sim = new QCTraceSimulator(traceSimCfg);
            var res = MyQuantumProgram.Run().Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

<span data-ttu-id="e1217-116">A classe `QCTraceSimulatorConfiguration` armazena a configuração do simulador de rastreamento do computador Quantum e pode ser fornecida como um argumento para o `QCTraceSimulator` Construtor.</span><span class="sxs-lookup"><span data-stu-id="e1217-116">The class `QCTraceSimulatorConfiguration` stores the configuration of the quantum computer trace simulator and can be provided as an argument for the `QCTraceSimulator` constructor.</span></span> <span data-ttu-id="e1217-117">Quando `useDistinctInputsChecker` é definido como true, o `Distinct Inputs Checker` é habilitado.</span><span class="sxs-lookup"><span data-stu-id="e1217-117">When `useDistinctInputsChecker` is set to true the `Distinct Inputs Checker` is enabled.</span></span> <span data-ttu-id="e1217-118">Consulte a documentação da API em [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) e [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration?) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="e1217-118">See the API documentation on [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) and [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration?) for more details.</span></span>

## <a name="see-also"></a><span data-ttu-id="e1217-119">Veja também</span><span class="sxs-lookup"><span data-stu-id="e1217-119">See also</span></span>

- <span data-ttu-id="e1217-120">A visão geral do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro) do computador Quantum.</span><span class="sxs-lookup"><span data-stu-id="e1217-120">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
