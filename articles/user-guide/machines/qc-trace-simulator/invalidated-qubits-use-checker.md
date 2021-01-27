---
title: Verificador de uso qubits invalidado – kit de desenvolvimento Quantum
description: Saiba mais sobre o verificador de uso qubits invalidado do Microsoft QDK, que usa o simulador de rastreamento Quantum para verificar o Q# código em busca de qubits potencialmente inválidos.
author: vadym-kl
ms.author: vadym
ms.date: 06/25/2020
ms.topic: conceptual
uid: microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits
no-loc:
- Q#
- $$v
ms.openlocfilehash: 9014097ace7c9f19d93a92372da40f71fa7f87ee
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858616"
---
# <a name="quantum-trace-simulator-invalidated-qubits-use-checker"></a>Simulador de rastreamento Quantum: verificador de uso invalidado do qubits

O verificador de uso invalidado do qubits faz parte do [simulador de rastreamento Quantum](xref:microsoft.quantum.machines.qc-trace-simulator.intro)do kit de desenvolvimento Quantum. Você pode usá-lo para detectar possíveis bugs no código causado por qubits inválidas. 

## <a name="invalid-qubits"></a>Qubits inválido

Considere o seguinte trecho de Q# código para ilustrar os problemas detectados pelo verificador de uso invalidado do qubits:

```qsharp
operation UseReleasedQubit() : Unit {
    mutable q = new Qubit[1];
    using (ans = Qubit()) {
        set q w/= 0 <- ans;
    }
    H(q[0]);
}
```

Quando você aplica a `H` operação ao `q[0]` , ele aponta para um qubit já liberado, o que pode causar um comportamento indefinido. Quando o verificador de uso invalidado do qubits estiver habilitado, ele lançará a exceção `InvalidatedQubitsUseCheckerException` se o programa aplicar uma operação a um qubit já liberado. Para obter mais informações, consulte <xref:Microsoft.Quantum.Simulation.QCTraceSimulatorRuntime.InvalidatedQubitsUseCheckerException>.

## <a name="invoking-the-invalidated-qubits-use-checker"></a>Invocando o verificador de uso qubits invalidado

Para executar o simulador de rastreamento do Quantum com o verificador de uso invalidado do qubits, você deve criar uma <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instância, definir a `UseInvalidatedQubitsUseChecker` propriedade como **true** e, em seguida, criar uma nova <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instância com `QCTraceSimulatorConfiguration` como o parâmetro. 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseInvalidatedQubitsUseChecker = true;
var sim = new QCTraceSimulator(config);
```


## <a name="using-the-invalidated-qubits-use-checker-in-a-c-host-program"></a>Usando o verificador de uso invalidado do qubits em um programa de host C#

Veja a seguir um exemplo de programas de host C# que usa o simulador de rastreamento Quantum com o verificador de uso invalidado do qubits habilitado: 

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

## <a name="see-also"></a>Confira também

- A visão geral do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro) do quantum do kit de desenvolvimento Quantum.
- A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> referência da API.
- A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> referência da API.
- A <xref:Microsoft.Quantum.Simulation.QCTraceSimulatorRuntime.InvalidatedQubitsUseCheckerException> referência da API.
