---
title: Qubits invalidados usam o verificador
description: 'Saiba mais sobre o verificador de uso qubits invalidado do Microsoft QDK, que verifica o código de Q # em busca de qubits potencialmente inválidos.'
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits
ms.openlocfilehash: e2bbb12448e27f28db030a0084302fb24f46f26b
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274259"
---
# <a name="invalidated-qubits-use-checker"></a>Verificador de uso qubits invalidado

O `Invalidated Qubits Use Checker` é uma parte do computador Quantum [TraceSimulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) projetado para detectar possíveis bugs no código. Considere a seguinte parte do código do Q # para ilustrar os problemas detectados pelo `Invalidated Qubits Use Checker` .

```qsharp
operation UseReleasedQubit() : Unit {
    mutable q = new Qubit[1];
    using (ans = Qubit()) {
        set q w/= 0 <- ans;
    }
    H(q[0]);
}
```

Quando `H` é aplicado a `q[0]` ele aponta para um qubit já liberado. Isso pode causar um comportamento indefinido. Quando o `Invalidated Qubits Use Checker` estiver habilitado, a exceção `InvalidatedQubitsUseCheckerException` será lançada se uma operação for aplicada a um qubit já liberado. Consulte a documentação da API em [InvalidatedQubitsUseCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException) para obter mais detalhes.

## <a name="using-the-invalidated-qubits-use-checker-in-your-c-program"></a>Usando o verificador de uso invalidado do qubits em seu programa C#

Veja a seguir um exemplo de código de driver C# para usar o computador Quantum `Trace
Simulator` com o `Invalidated Qubits Use Checker` habilitado: 

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

A classe `QCTraceSimulatorConfiguration` armazena a configuração do simulador de rastreamento do computador Quantum e pode ser fornecida como um argumento para o `QCTraceSimulator` Construtor. Quando `useInvalidatedQubitsUseChecker` é definido como true, o `Invalidated Qubits Use Checker` é habilitado. Consulte a documentação da API em [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) e [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) para obter mais detalhes.

## <a name="see-also"></a>Veja também ##

- A visão geral do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro) do computador Quantum.
