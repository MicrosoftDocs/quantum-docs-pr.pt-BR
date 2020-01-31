---
title: Verificador de entradas distintos | Simulador de rastreamento de computador Quantum | Microsoft Docs
description: Visão geral do simulador de rastreamento de computador quântico
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.distinct-inputs
ms.openlocfilehash: 3c21a54f5da83bf1ea0792e79cc773be5fba71e8
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820956"
---
# <a name="distinct-inputs-checker"></a>Verificador de entradas distintos

O `Distinct Inputs Checker` é uma parte do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro)de computador Quantum. Ele foi projetado para detectar possíveis bugs no código. Considere a seguinte parte do código do Q # para ilustrar os problemas detectados por este pacote:

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

Quando o usuário examina esse programa, ele pressupõe que a ordem na qual `op1` e `op2` são chamados não importa porque `q1` e `q2` são diferentes qubits e operações que atuam em diferentes qubits. Agora, vamos considerar um exemplo, em que esta operação é usada:

```qsharp
operation ApplyWithNonDistinctInputs() : Unit {
    using (qubits = Qubit[3]) {
        let op1 = CNOT(_, qubits[1]);
        let op2 = CNOT(qubits[1], _);
        ApplyBoth(qubits[0], qubits[2], op1, op2);
    }
}
```

Agora `op1` e `op2` são obtidos usando o aplicativo parcial e compartilham um qubit. Quando o usuário chama `ApplyBoth` no exemplo acima, o resultado da operação dependerá da ordem de `op1` e `op2` dentro `ApplyBoth`. Isso definitivamente não é o que o usuário esperaria acontecer. O `Distinct Inputs Checker` detectará essas situações quando habilitado e gerará `DistinctInputsCheckerException`. Consulte a documentação da API em [DistinctInputsCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException) para obter mais detalhes.

## <a name="using-the-distinct-inputs-checker-in-your-c-program"></a>Usando o verificador de entradas distintos em seu C# programa

Veja a seguir um exemplo de C# código de driver para usar o simulador de rastreamento de computador Quantum com o `Distinct Inputs Checker` habilitado:

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

A classe `QCTraceSimulatorConfiguration` armazena a configuração do simulador de rastreamento do computador Quantum e pode ser fornecida como um argumento para o Construtor `QCTraceSimulator`. Quando `useDistinctInputsChecker` é definido como true, o `Distinct Inputs Checker` está habilitado. Consulte a documentação da API em [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) e [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration?) para obter mais detalhes.

## <a name="see-also"></a>Consulte também

- A visão geral do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro) do computador Quantum.
