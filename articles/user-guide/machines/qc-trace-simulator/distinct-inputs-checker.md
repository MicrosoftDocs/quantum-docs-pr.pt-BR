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

Quando o usuário examina esse programa, ele pressupõe que a ordem na qual `op1` e `op2` são chamados não importa porque `q1` e `q2` são qubits diferentes e operações que atuam em qubits diferentes. Agora, vamos considerar um exemplo, em que esta operação é usada:

```qsharp
operation ApplyWithNonDistinctInputs() : Unit {
    using (qubits = Qubit[3]) {
        let op1 = CNOT(_, qubits[1]);
        let op2 = CNOT(qubits[1], _);
        ApplyBoth(qubits[0], qubits[2], op1, op2);
    }
}
```

Agora `op1` , `op2` ambos são obtidos usando o aplicativo parcial e compartilham um qubit. Quando o usuário chama `ApplyBoth` no exemplo acima, o resultado da operação dependerá da ordem de `op1` e `op2` dentro `ApplyBoth` . Isso definitivamente não é o que o usuário esperaria acontecer. O `Distinct Inputs Checker` detectará essas situações quando for habilitado e gerará `DistinctInputsCheckerException` . Consulte a documentação da API em [DistinctInputsCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException) para obter mais detalhes.

## <a name="using-the-distinct-inputs-checker-in-your-c-program"></a>Usando o verificador de entradas distintos em seu programa C#

Veja a seguir um exemplo de código de driver C# para usar o simulador de rastreamento de computador Quantum com o `Distinct Inputs Checker` habilitado:

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

A classe `QCTraceSimulatorConfiguration` armazena a configuração do simulador de rastreamento do computador Quantum e pode ser fornecida como um argumento para o `QCTraceSimulator` Construtor. Quando `useDistinctInputsChecker` é definido como true, o `Distinct Inputs Checker` é habilitado. Consulte a documentação da API em [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) e [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration?) para obter mais detalhes.

## <a name="see-also"></a>Veja também

- A visão geral do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro) do computador Quantum.
