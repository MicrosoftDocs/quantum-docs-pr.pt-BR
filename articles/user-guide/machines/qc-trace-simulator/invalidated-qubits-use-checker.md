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
# <a name="quantum-trace-simulator-invalidated-qubits-use-checker"></a>Simulador de rastreamento Quantum: verificador de uso invalidado do qubits

O verificador de uso invalidado do qubits faz parte do [simulador de rastreamento Quantum](xref:microsoft.quantum.machines.qc-trace-simulator.intro)do kit de desenvolvimento Quantum. Você pode usá-lo para detectar possíveis bugs no código causado por qubits inválidas. 

## <a name="invalid-qubits"></a>Qubits inválido

Considere a seguinte parte do código do Q # para ilustrar os problemas detectados pelo verificador de uso invalidado do qubits:

```qsharp
operation UseReleasedQubit() : Unit {
    mutable q = new Qubit[1];
    using (ans = Qubit()) {
        set q w/= 0 <- ans;
    }
    H(q[0]);
}
```

Quando você aplica a `H` operação ao `q[0]` , ele aponta para um qubit já liberado, o que pode causar um comportamento indefinido. Quando o verificador de uso invalidado do qubits estiver habilitado, ele lançará a exceção `InvalidatedQubitsUseCheckerException` se o programa aplicar uma operação a um qubit já liberado. Para obter mais informações, consulte <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException>.

## <a name="invoking-the-invalidated-qubits-use-checker"></a>Invocando o verificador de uso qubits invalidado

Para executar o simulador de rastreamento do Quantum com o verificador de uso invalidado do qubits, você deve criar uma <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instância, definir a `UseInvalidatedQubitsUseChecker` propriedade como **true**e, em seguida, criar uma nova <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instância com `QCTraceSimulatorConfiguration` como o parâmetro. 

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

## <a name="see-also"></a>Veja também

- A visão geral do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro) do quantum do kit de desenvolvimento Quantum.
- A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> referência da API.
- A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> referência da API.
- A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException> referência da API.