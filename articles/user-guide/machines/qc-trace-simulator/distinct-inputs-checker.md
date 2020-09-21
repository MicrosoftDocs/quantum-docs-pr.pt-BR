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
# <a name="quantum-trace-simulator-distinct-inputs-checker"></a>Simulador de rastreamento Quantum: verificador de entradas distintos

O verificador de entradas distintos faz parte do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro)Quantum do kit de desenvolvimento Quantum. Você pode usá-lo para detectar possíveis bugs no código causado por conflitos com qubits compartilhados. 

## <a name="conflicts-with-shared-qubits"></a>Conflitos com qubits compartilhados

Considere o seguinte trecho de Q# código para ilustrar os problemas detectados pelo verificador de entradas distintos:

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

Ao examinar esse programa, você pode assumir que a ordem em que ele chama e não `op1` `op2` importa, porque `q1` e `q2` são diferentes qubits e operações que atuam em diferentes qubits. 

Agora, considere este exemplo:

```qsharp
operation ApplyWithNonDistinctInputs() : Unit {
    using (qubits = Qubit[3]) {
        let op1 = CNOT(_, qubits[1]);
        let op2 = CNOT(qubits[1], _);
        ApplyBoth(qubits[0], qubits[2], op1, op2);
    }
}
```

Observe que `op1` e `op2` são obtidos usando o aplicativo parcial e compartilham um qubit. Quando você chama `ApplyBoth` neste exemplo, o resultado da operação depende da ordem de `op1` e `op2` dentro `ApplyBoth` , não é o que você esperaria acontecer. Quando você habilita o verificador de entradas distintos, ele detecta essas situações e gera um `DistinctInputsCheckerException` . Para obter mais informações, consulte <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException> na Q# biblioteca de API.

## <a name="invoking-the-distinct-inputs-checker"></a>Invocando o verificador de entradas distintos

Para executar o simulador de rastreamento do Quantum com o verificador de entradas distintos, você deve criar uma <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instância, definir a `UseDistinctInputsChecker` propriedade como **true**e, em seguida, criar uma nova <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instância com `QCTraceSimulatorConfiguration` como o parâmetro. 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseDistinctInputsChecker = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-distinct-inputs-checker-in-a-c-host-program"></a>Usando o verificador de entradas distintos em um programa de host C#

Veja a seguir um exemplo de programa de host C# que usa o simulador de rastreamento Quantum com o verificador de entradas distintos habilitado:

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

## <a name="see-also"></a>Consulte também

- A visão geral do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro) do quantum do kit de desenvolvimento Quantum.
- A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> referência da API.
- A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> referência da API.
- A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException> referência da API.
