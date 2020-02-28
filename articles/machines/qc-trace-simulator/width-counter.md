---
title: Contador de largura
description: Saiba mais sobre o contador de largura QDK da Microsoft, que conta o número de qubits alocadas e emprestadas por cada operação em um programa Quantum.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.width-counter
ms.openlocfilehash: a76292222950310acc90dded02980e4a5b792e76
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907079"
---
# <a name="width-counter"></a>Contador de largura

O `Width Counter` conta o número de qubits alocados e emprestados por cada operação.
Todas as operações do namespace `Microsoft.Quantum.Intrinsic` são expressas em termos de rotações qubit únicas, T Gates, Single qubit Clifford Gates, CNOT Gates e medidas de qubit de vários Pauli observáveis. Algumas das operações primitivas podem alocar qubits extras. Por exemplo, multiplique `X` Gates controlado ou Gates de `T` controlado. Vamos calcular o número de qubits extras alocados pela implementação de um portão de `X` controlado por multiplicação:

```qsharp
open Microsoft.Quantum.Intrinsic;
open Microsoft.Quantum.Arrays;
operation ApplyMultiControlledX( numberOfQubits : Int ) : Unit {
    using(qubits = Qubit[numberOfQubits]) {
        Controlled X (Rest(qubits), Head(qubits));
    } 
}
```

## <a name="using-width-counter-within-a-c-program"></a>Usando o contador de largura C# dentro de um programa

Multiplicar `X` controlado atuando em um total de 5 qubits alocará 2 qubits auxiliares e sua largura de entrada será 5. Para verificar se esse é o caso, podemos usar o seguinte C# programa:

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

A primeira parte do programa executa `ApplyMultiControlledX`. Na segunda parte, usamos o método `QCTraceSimulator.GetMetric` para obter o número de qubits alocadas, bem como o número de qubits que controlavam `X` recebido como entrada. 

Por fim, para gerar todas as estatísticas coletadas pelo contador de largura no formato CSV, podemos usar o seguinte:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.widthCounter];
```

## <a name="see-also"></a>Consulte também ##

- A visão geral do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro) do computador Quantum.
