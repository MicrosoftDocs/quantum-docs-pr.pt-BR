---
title: Contador de largura – kit de desenvolvimento do Quantum
description: 'Saiba mais sobre o contador de largura QDK da Microsoft, que usa o simulador de rastreamento Quantum para contar o número de qubits alocados e emprestados por operações em um programa Q #.'
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.width-counter
ms.openlocfilehash: af8609dc5c05f7a19b8d21755281427feb29b84c
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871511"
---
# <a name="quantum-trace-simulator-width-counter"></a>Simulador de rastreamento Quantum: contador de largura

O contador de largura faz parte do [simulador de rastreamento Quantum](xref:microsoft.quantum.machines.qc-trace-simulator.intro)do kit de desenvolvimento Quantum. Você pode usá-lo para contar o número de qubits alocadas e emprestadas por cada operação em um programa Q #. Algumas operações primitivas podem alocar qubits extras, por exemplo, operações controladas multiplicadas `X` ou operações controladas `T` .

## <a name="invoking-the-width-counter"></a>Invocando o contador de largura

Para executar o simulador de rastreamento do Quantum com o contador de largura, você deve criar uma <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instância, definir a `UseWidthCounter` propriedade como **true**e, em seguida, criar uma nova <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instância com o `QCTraceSimulatorConfiguration` como o parâmetro. 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseWidthCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-width-counter-in-a-c-host-program"></a>Usando o contador de largura em um programa de host C#

O exemplo de C# a seguir nesta seção computa o número de qubits extras alocados pela implementação de uma operação controlada de multiplicação <xref:microsoft.quantum.intrinsic.x> , com base no seguinte código de exemplo de p #:

```qsharp
open Microsoft.Quantum.Intrinsic;
open Microsoft.Quantum.Arrays;
operation ApplyMultiControlledX( numberOfQubits : Int ) : Unit {
    using(qubits = Qubit[numberOfQubits]) {
        Controlled X (Rest(qubits), Head(qubits));
    } 
}
```

A operação de multiplicação controlada <xref:microsoft.quantum.intrinsic.x> atua em um total de cinco qubits, aloca dois [qubits auxiliares](xref:microsoft.quantum.glossary#ancilla)e tem uma largura de entrada de **5**. Use o seguinte programa C# para verificar as contagens:

```csharp 
var config = new QCTraceSimulatorConfiguration();
config.UseWidthCounter = true;
var sim = new QCTraceSimulator(config);
int totalNumberOfQubits = 5;
var res = ApplyMultiControlledX.Run(sim, totalNumberOfQubits).Result;

double allocatedQubits = 
    sim.GetMetric<Primitive.X, ApplyMultiControlledX>(
        WidthCounter.Metrics.ExtraWidth,
        functor: OperationFunctor.Controlled); 

double inputWidth =
    sim.GetMetric<Primitive.X, ApplyMultiControlledX>(
        WidthCounter.Metrics.InputWidth,
        functor: OperationFunctor.Controlled);
```

A primeira parte do programa executa a `ApplyMultiControlledX` operação. A segunda parte usa o [`QCTraceSimulator.GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) método para recuperar o número de qubits alocadas, bem como o número de qubits que a `Controlled X` operação recebeu como entrada. 

Por fim, você pode gerar todas as estatísticas coletadas pelo contador de largura no formato CSV usando o seguinte:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.widthCounter];
```

## <a name="see-also"></a>Veja também

- A visão geral do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro) do quantum do kit de desenvolvimento Quantum.
- A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> referência da API.
- A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> referência da API.
- A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.WidthCounter> referência da API.
