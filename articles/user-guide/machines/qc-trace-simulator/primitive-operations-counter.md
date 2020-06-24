---
title: Contador de operações primitivas
description: Saiba mais sobre o contador de operações do Microsoft QDK Primitive, que controla o número de execuções primitivas usadas pelas operações em um programa Quantum.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.primitive-counter
ms.openlocfilehash: 8bdb0aed370e72b58b23025f1685ad7ce1a77a43
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274257"
---
# <a name="primitive-operations-counter"></a>Contador de operações primitivas  

O `Primitive Operations Counter` é uma parte do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro)de computador Quantum. Ele conta o número de execuções primitivas usadas por cada operação invocada em um programa Quantum. Todas as operações do `Microsoft.Quantum.Intrinsic` são expressas em termos de rotações qubit únicas, T Gates, Single qubit Clifford Gates, CNOT Gates e medidas de qubit de vários Pauli observáveis. As estatísticas coletadas são agregadas nas bordas do grafo de chamada de operações. Agora, vamos contar quantas `T` Gates são necessárias para implementar a `CCNOT` operação. 

```qsharp
open Microsoft.Quantum.Intrinsic;
operation ApplySampleWithCCNOT() : Unit {

    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    } 
}
```

## <a name="using-the-primitive-operations-counter-within-a-c-program"></a>Usando o contador de operações primitivas em um programa C#

Para verificar se `CCNOT` realmente requer 7 `T` Gates e que `ApplySampleWithCCNOT` Execute 8 `T` Gates, podemos usar o seguinte código C#:

```csharp 
// using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
// using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.usePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tCountAll = sim.GetMetric<ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
double tCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
```

A primeira parte do programa é executada `ApplySampleWithCCNOT` . Na segunda parte, usamos o método `QCTraceSimulator.GetMetric` para obter o número de T Gates executadas por `ApplySampleWithCCNOT` : 

```csharp
double tCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
double tCountAll = sim.GetMetric<ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
```

Quando `GetMetric` é chamado com dois parâmetros de tipo, ele retorna o valor da métrica associada a uma determinada borda de gráfico de chamada. Em nossa operação de exemplo `Primitive.CCNOT` é chamada dentro `ApplySampleWithCCNOT` e, portanto, o grafo de chamada contém a borda `<Primitive.CCNOT, ApplySampleWithCCNOT>` . 

Para obter o número de `CNOT` Gates usadas, podemos adicionar a seguinte linha:
```csharp
double cxCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.CX);
```

Por fim, para gerar todas as estatísticas coletadas pelo contador portão no formato CSV, podemos usar o seguinte:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.primitiveOperationsCounter];
```

## <a name="see-also"></a>Veja também ##

- A visão geral do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro) do computador Quantum.
