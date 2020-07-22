---
title: Verificador de uso qubits invalidado – kit de desenvolvimento Quantum
description: 'Saiba mais sobre o verificador de uso qubits invalidado do Microsoft QDK, que usa o simulador de rastreamento do Quantum para verificar o código de Q # para qubits potencialmente inválidos.'
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits
ms.openlocfilehash: fccf6d5784b587f4ad9b659e23027619acd06ffa
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871086"
---
# <a name="quantum-trace-simulator-invalidated-qubits-use-checker"></a><span data-ttu-id="2d15e-103">Simulador de rastreamento Quantum: verificador de uso invalidado do qubits</span><span class="sxs-lookup"><span data-stu-id="2d15e-103">Quantum trace simulator: invalidated qubits use checker</span></span>

<span data-ttu-id="2d15e-104">O verificador de uso invalidado do qubits faz parte do [simulador de rastreamento Quantum](xref:microsoft.quantum.machines.qc-trace-simulator.intro)do kit de desenvolvimento Quantum.</span><span class="sxs-lookup"><span data-stu-id="2d15e-104">The invalidated qubits use checker is a part of the Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="2d15e-105">Você pode usá-lo para detectar possíveis bugs no código causado por qubits inválidas.</span><span class="sxs-lookup"><span data-stu-id="2d15e-105">You can use it to detect potential bugs in the code caused by invalid qubits.</span></span> 

## <a name="invalid-qubits"></a><span data-ttu-id="2d15e-106">Qubits inválido</span><span class="sxs-lookup"><span data-stu-id="2d15e-106">Invalid qubits</span></span>

<span data-ttu-id="2d15e-107">Considere a seguinte parte do código do Q # para ilustrar os problemas detectados pelo verificador de uso invalidado do qubits:</span><span class="sxs-lookup"><span data-stu-id="2d15e-107">Consider the following piece of Q# code to illustrate the issues detected by the invalidated qubits use checker:</span></span>

```qsharp
operation UseReleasedQubit() : Unit {
    mutable q = new Qubit[1];
    using (ans = Qubit()) {
        set q w/= 0 <- ans;
    }
    H(q[0]);
}
```

<span data-ttu-id="2d15e-108">Quando você aplica a `H` operação ao `q[0]` , ele aponta para um qubit já liberado, o que pode causar um comportamento indefinido.</span><span class="sxs-lookup"><span data-stu-id="2d15e-108">When you apply the `H` operation to `q[0]`, it points to an already released qubit, which can cause undefined behavior.</span></span> <span data-ttu-id="2d15e-109">Quando o verificador de uso invalidado do qubits estiver habilitado, ele lançará a exceção `InvalidatedQubitsUseCheckerException` se o programa aplicar uma operação a um qubit já liberado.</span><span class="sxs-lookup"><span data-stu-id="2d15e-109">When the Invalidated Qubits Use Checker is enabled, it throws the exception `InvalidatedQubitsUseCheckerException` if the program applies an operation to an already released qubit.</span></span> <span data-ttu-id="2d15e-110">Para obter mais informações, consulte <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException>.</span><span class="sxs-lookup"><span data-stu-id="2d15e-110">For more information, see <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException>.</span></span>

## <a name="invoking-the-invalidated-qubits-use-checker"></a><span data-ttu-id="2d15e-111">Invocando o verificador de uso qubits invalidado</span><span class="sxs-lookup"><span data-stu-id="2d15e-111">Invoking the invalidated qubits use checker</span></span>

<span data-ttu-id="2d15e-112">Para executar o simulador de rastreamento do Quantum com o verificador de uso invalidado do qubits, você deve criar uma <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instância, definir a `UseInvalidatedQubitsUseChecker` propriedade como **true**e, em seguida, criar uma nova <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instância com `QCTraceSimulatorConfiguration` como o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="2d15e-112">To run the quantum trace simulator with the invalidated qubits use checker you must create a <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instance, set the `UseInvalidatedQubitsUseChecker` property to **true**, and then create a new <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instance with `QCTraceSimulatorConfiguration` as the parameter.</span></span> 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseInvalidatedQubitsUseChecker = true;
var sim = new QCTraceSimulator(config);
```


## <a name="using-the-invalidated-qubits-use-checker-in-a-c-host-program"></a><span data-ttu-id="2d15e-113">Usando o verificador de uso invalidado do qubits em um programa de host C#</span><span class="sxs-lookup"><span data-stu-id="2d15e-113">Using the invalidated qubits use checker in a C# host program</span></span>

<span data-ttu-id="2d15e-114">Veja a seguir um exemplo de programas de host C# que usa o simulador de rastreamento Quantum com o verificador de uso invalidado do qubits habilitado:</span><span class="sxs-lookup"><span data-stu-id="2d15e-114">The following is an example of C# host programs that uses the quantum trace simulator with the invalidated qubits use checker enabled:</span></span> 

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
            traceSimCfg.UseInvalidatedQubitsUseChecker = true; // enables UseInvalidatedQubitsUseChecker
            QCTraceSimulator sim = new QCTraceSimulator(traceSimCfg);
            var res = MyQuantumProgram.Run().Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="2d15e-115">Veja também</span><span class="sxs-lookup"><span data-stu-id="2d15e-115">See also</span></span>

- <span data-ttu-id="2d15e-116">A visão geral do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro) do quantum do kit de desenvolvimento Quantum.</span><span class="sxs-lookup"><span data-stu-id="2d15e-116">The Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
- <span data-ttu-id="2d15e-117">A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> referência da API.</span><span class="sxs-lookup"><span data-stu-id="2d15e-117">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API reference.</span></span>
- <span data-ttu-id="2d15e-118">A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> referência da API.</span><span class="sxs-lookup"><span data-stu-id="2d15e-118">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API reference.</span></span>
- <span data-ttu-id="2d15e-119">A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException> referência da API.</span><span class="sxs-lookup"><span data-stu-id="2d15e-119">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException> API reference.</span></span>