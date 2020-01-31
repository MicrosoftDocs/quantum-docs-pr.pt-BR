---
title: Verificador de uso qubits invalidado | Simulador de rastreamento de computador Quantum | Microsoft Docs
description: Visão geral do simulador de rastreamento de computador quântico
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits
ms.openlocfilehash: 093937346488725eacb69ef7da6affde764ec5c1
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820871"
---
# <a name="invalidated-qubits-use-checker"></a><span data-ttu-id="9e051-103">Verificador de uso qubits invalidado</span><span class="sxs-lookup"><span data-stu-id="9e051-103">Invalidated Qubits Use Checker</span></span>

<span data-ttu-id="9e051-104">O `Invalidated Qubits Use Checker` é uma parte do computador Quantum [TraceSimulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) projetado para detectar possíveis bugs no código.</span><span class="sxs-lookup"><span data-stu-id="9e051-104">The `Invalidated Qubits Use Checker` is a part of the quantum computer [TraceSimulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) designed for detecting potential bugs in the code.</span></span> <span data-ttu-id="9e051-105">Considere a seguinte parte do código do Q # para ilustrar os problemas detectados pelo `Invalidated Qubits Use Checker`.</span><span class="sxs-lookup"><span data-stu-id="9e051-105">Consider the following piece of Q# code to illustrate the issues detected by the `Invalidated Qubits Use Checker`.</span></span>

```qsharp
operation UseReleasedQubit() : Unit {
    mutable q = new Qubit[1];
    using (ans = Qubit()) {
        set q w/= 0 <- ans;
    }
    H(q[0]);
}
```

<span data-ttu-id="9e051-106">Quando `H` é aplicado a `q[0]` aponta para um qubit já liberado.</span><span class="sxs-lookup"><span data-stu-id="9e051-106">When `H` is applied to `q[0]` it points to an already released qubit.</span></span> <span data-ttu-id="9e051-107">Isso pode causar um comportamento indefinido.</span><span class="sxs-lookup"><span data-stu-id="9e051-107">This can cause undefined behavior.</span></span> <span data-ttu-id="9e051-108">Quando a `Invalidated Qubits Use Checker` estiver habilitada, a exceção `InvalidatedQubitsUseCheckerException` será lançada se uma operação for aplicada a um qubit já liberado.</span><span class="sxs-lookup"><span data-stu-id="9e051-108">When the `Invalidated Qubits Use Checker` is enabled, the exception `InvalidatedQubitsUseCheckerException` will be thrown if an operation is applied to an already released qubit.</span></span> <span data-ttu-id="9e051-109">Consulte a documentação da API em [InvalidatedQubitsUseCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="9e051-109">See the API documentation on [InvalidatedQubitsUseCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException) for more details.</span></span>

## <a name="using-the-invalidated-qubits-use-checker-in-your-c-program"></a><span data-ttu-id="9e051-110">Usando o verificador de uso invalidado do C# qubits em seu programa</span><span class="sxs-lookup"><span data-stu-id="9e051-110">Using the Invalidated Qubits Use Checker in your C# Program</span></span>

<span data-ttu-id="9e051-111">Veja a seguir um exemplo de C# código de driver para usar o computador Quantum `Trace
Simulator` com o `Invalidated Qubits Use Checker` habilitado:</span><span class="sxs-lookup"><span data-stu-id="9e051-111">The following is an example of C# driver code for using the quantum computer `Trace
Simulator` with the `Invalidated Qubits Use Checker` enabled:</span></span> 

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
            traceSimCfg.useInvalidatedQubitsUseChecker = true; // enables useInvalidatedQubitsUseChecker
            QCTraceSimulator sim = new QCTraceSimulator(traceSimCfg);
            var res = MyQuantumProgram.Run().Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

<span data-ttu-id="9e051-112">A classe `QCTraceSimulatorConfiguration` armazena a configuração do simulador de rastreamento do computador Quantum e pode ser fornecida como um argumento para o Construtor `QCTraceSimulator`.</span><span class="sxs-lookup"><span data-stu-id="9e051-112">The class `QCTraceSimulatorConfiguration` stores the configuration of the quantum computer trace simulator and can be provided as an argument for the `QCTraceSimulator` constructor.</span></span> <span data-ttu-id="9e051-113">Quando `useInvalidatedQubitsUseChecker` é definido como true, o `Invalidated Qubits Use Checker` está habilitado.</span><span class="sxs-lookup"><span data-stu-id="9e051-113">When `useInvalidatedQubitsUseChecker` is set to true the `Invalidated Qubits Use Checker` is enabled.</span></span> <span data-ttu-id="9e051-114">Consulte a documentação da API em [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) e [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="9e051-114">See the API documentation on [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) and [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) for more details.</span></span>

## <a name="see-also"></a><span data-ttu-id="9e051-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9e051-115">See also</span></span> ##

- <span data-ttu-id="9e051-116">A visão geral do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro) do computador Quantum.</span><span class="sxs-lookup"><span data-stu-id="9e051-116">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
