---
title: Contador de profundidade
description: Saiba mais sobre o contador de profundidade do Microsoft QDK, que reúne as contagens da profundidade de cada operação invocada em um programa Quantum.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.depth-counter
ms.openlocfilehash: d532a9f512b8c87d83d62ed26e3bb67e1b6f668b
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/28/2020
ms.locfileid: "77906093"
---
# <a name="depth-counter"></a>Contador de profundidade

O `Depth Counter` é uma parte do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro)de computador Quantum.
Ele é usado para reunir contagens da profundidade de cada operação invocada em um programa Quantum. Todas as operações de <xref:microsoft.quantum.intrinsic> são expressas em termos de rotações qubit únicas, T Gates, Single qubit Clifford Gates, CNOT Gates e medidas de qubit de vários Pauli observáveis. Os usuários podem definir a profundidade para cada uma das operações primitivas por meio do campo `gateTimes` de <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>.

Por padrão, todas as operações têm profundidade 0, exceto o portão T que tem profundidade 1. Isso significa que, por padrão, somente a profundidade de operações T é calculada (o que geralmente é desejável). As estatísticas coletadas são agregadas em todas as bordas do grafo de chamada de operações. 

Agora, vamos calcular a profundidade de <xref:microsoft.quantum.intrinsic.t> da operação <xref:microsoft.quantum.intrinsic.ccnot>. Usaremos o seguinte código de exemplo de Q #:

```qsharp
open Microsoft.Quantum.Intrinsic;

operation ApplySampleWithCCNOT() : Unit {
    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

## <a name="using-depth-counter-within-a-c-program"></a>Usando o contador de profundidade C# em um programa

Para verificar se `CCNOT` tem `T` profundidade 5 e `ApplySampleWithCCNOT` tem `T` profundidade 6, podemos usar o seguinte C# código:

```csharp
using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.useDepthCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tDepth = sim.GetMetric<Intrinsic.CCNOT, ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
```

A primeira parte do programa executa `ApplySampleWithCCNOT`. Na segunda parte, usamos o método `QCTraceSimulator.GetMetric` para obter a profundidade de `T` de `CCNOT` e `ApplySampleWithCCNOT`: 

```csharp
double tDepth = sim.GetMetric<Intrinsic.CCNOT, ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
```

Por fim, para gerar todas as estatísticas coletadas por `Depth Counter` no formato CSV, podemos usar o seguinte:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.depthCounter];
```

## <a name="see-also"></a>Consulte também ##

- A visão geral do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro) do computador Quantum.
