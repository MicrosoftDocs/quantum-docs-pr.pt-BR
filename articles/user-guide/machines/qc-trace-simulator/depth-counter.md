---
title: Contador de profundidade – kit de desenvolvimento do Quantum
description: 'Saiba mais sobre o contador de profundidade do Microsoft QDK, que usa o simulador de rastreamento do Quantum para reunir contagens da profundidade de cada operação invocada em um programa Q #.'
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.depth-counter
ms.openlocfilehash: 811e387fedf547d2681518ae0bb525c13dc84ff4
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871120"
---
# <a name="quantum-trace-simulator-depth-counter"></a>Simulador de rastreamento Quantum: contador de profundidade

O contador de profundidade faz parte do [simulador de rastreamento Quantum](xref:microsoft.quantum.machines.qc-trace-simulator.intro)do kit de desenvolvimento Quantum.
Você pode usá-lo para reunir contagens que representam o limite inferior da profundidade de cada operação invocada em um programa Quantum. 

## <a name="depth-values"></a>Valores de profundidade

Por padrão, todas as operações têm uma profundidade de **0** , exceto a `T` operação, que tem uma profundidade de **1**. Isso significa que, por padrão, apenas a `T` profundidade das operações é computada (o que geralmente é desejável). O contador de profundidade agrega e coleta estatísticas sobre todas as bordas do [grafo de chamada](https://en.wikipedia.org/wiki/Call_graph)da operação.

Todas as <xref:microsoft.quantum.intrinsic> operações são expressas em termos de rotações de qubit único, operações <xref:microsoft.quantum.intrinsic.t> , operações de Clifford de qubit único, <xref:microsoft.quantum.intrinsic.cnot> operações e medidas de Pauli de vários qubit observáveis. Os usuários podem definir a profundidade para cada uma das operações primitivas por meio do `gateTimes` campo de <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> .

## <a name="invoking-the-depth-counter"></a>Invocando o contador de profundidade

Para executar o simulador de rastreamento Quantum com o contador de profundidade, você deve criar uma <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instância, definir sua `UseDepthCounter` propriedade como **true**e, em seguida, criar uma nova <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instância com `QCTraceSimulatorConfiguration` como o parâmetro. 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseDepthCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-depth-counter-in-a-c-host-program"></a>Usando o contador de profundidade em um programa de host C#

O exemplo de C# a seguir nesta seção computa a `T` profundidade da `CCNOT` operação, com base no seguinte código de exemplo de Q #:

```qsharp
open Microsoft.Quantum.Intrinsic;

operation ApplySampleWithCCNOT() : Unit {
    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

Para verificar se `CCNOT` `T` o tem profundidade **5** e `ApplySampleWithCCNOT` tem `T` profundidade **6**, use o seguinte código C#:

```csharp
using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.UseDepthCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tDepth = sim.GetMetric<Intrinsic.CCNOT, ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
```

A primeira parte do programa é executada `ApplySampleWithCCNOT` . A segunda parte usa o [`GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) método para recuperar a `T` profundidade de `CCNOT` e `ApplySampleWithCCNOT` . 

Por fim, você pode gerar todas as estatísticas coletadas pelo contador de profundidade no formato CSV usando o seguinte:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.depthCounter];
```

## <a name="see-also"></a>Veja também

- A visão geral do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro) do quantum do kit de desenvolvimento Quantum.
- A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> referência da API.
- A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> referência da API.
- A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.DepthCounter> referência da API.
