---
title: Contador de largura
description: Saiba mais sobre o contador de largura QDK da Microsoft, que conta o número de qubits alocadas e emprestadas por cada operação em um programa Quantum.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.width-counter
ms.openlocfilehash: a76292222950310acc90dded02980e4a5b792e76
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274258"
---
# <a name="width-counter"></a>Contador de largura

O `Width Counter` conta o número de qubits alocados e emprestados por cada operação.
Todas as operações do `Microsoft.Quantum.Intrinsic` namespace são expressas em termos de rotações de qubit únicas, T Gates, Single qubit Clifford Gates, CNOT Gates e medidas de qubit de vários Pauli observáveis. Algumas das operações primitivas podem alocar qubits extras. Por exemplo, multiplique as `X` Gates controladas ou as Gates controladas `T` . Vamos calcular o número de qubits extras alocados pela implementação de um portão com controle de multiplicação `X` :

```qsharp
open Microsoft.Quantum.Intrinsic;
open Microsoft.Quantum.Arrays;
operation ApplyMultiControlledX( numberOfQubits : Int ) : Unit {
    using(qubits = Qubit[numberOfQubits]) {
        Controlled X (Rest(qubits), Head(qubits));
    } 
}
```

## <a name="using-width-counter-within-a-c-program"></a>Usando o contador de largura em um programa C#

A multiplicação controlada `X` atuando em um total de 5 qubits alocará 2 qubits auxiliares e sua largura de entrada será 5. Para verificar se esse é o caso, podemos usar o seguinte programa C#:

```csharp 
var config = new QCTraceSimulatorConfiguration();
config.useWidthCounter = true;
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

A primeira parte do programa é executada `ApplyMultiControlledX` . Na segunda parte, usamos o método `QCTraceSimulator.GetMetric` para obter o número de qubits alocadas, bem como o número de qubits que são controlados `X` como entrada. 

Por fim, para gerar todas as estatísticas coletadas pelo contador de largura no formato CSV, podemos usar o seguinte:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.widthCounter];
```

## <a name="see-also"></a>Veja também ##

- A visão geral do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro) do computador Quantum.
