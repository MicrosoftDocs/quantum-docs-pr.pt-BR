---
title: Contador de operações primitivas – kit de desenvolvimento do Quantum
description: Saiba mais sobre o contador de operações do Microsoft QDK Primitive, que usa o simulador de rastreamento do Quantum para rastrear as execuções primitivas usadas pelas operações em um Q# programa.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.primitive-counter
no-loc:
- Q#
- $$v
ms.openlocfilehash: ceb70cef6dc0a4530b992b5a529248a8b283c17f
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868229"
---
# <a name="quantum-trace-simulator-primitive-operations-counter"></a>Simulador de rastreamento Quantum: contador de operações primitivas

O contador de operação primitiva é uma parte do [simulador de rastreamento Quantum](xref:microsoft.quantum.machines.qc-trace-simulator.intro)do kit de desenvolvimento Quantum. Ele conta o número de execuções primitivas usadas por cada operação invocada em um programa Quantum. 

Todas as <xref:microsoft.quantum.intrinsic> operações são expressas em termos de rotações de qubit único, operações de T, operações de Clifford de qubit único, operações de CNOT e medidas de qubit de vários Pauli observáveis. O contador de operações primitivas agrega e coleta estatísticas sobre todas as bordas do [grafo de chamada](https://en.wikipedia.org/wiki/Call_graph)da operação.

## <a name="invoking-the-primitive-operation-counter"></a>Invocando o contador de operação primitiva

Para executar o simulador de rastreamento do Quantum com o contador de operação primitiva, você deve criar uma <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instância, definir a `UsePrimitiveOperationsCounter` propriedade como **true**e, em seguida, criar uma nova <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instância com o `QCTraceSimulatorConfiguration` como o parâmetro.

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UsePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-primitive-operation-counter-in-a-c-host-program"></a>Usando o contador de operação primitiva em um programa de host C#

O exemplo de C# a seguir nesta seção conta quantas <xref:microsoft.quantum.intrinsic.t> operações são necessárias para implementar a <xref:microsoft.quantum.intrinsic.ccnot> operação, com base no seguinte Q# código de exemplo:

```qsharp
open Microsoft.Quantum.Intrinsic;
operation ApplySampleWithCCNOT() : Unit {

    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

Para verificar se `CCNOT` o requer sete `T` operações e que `ApplySampleWithCCNOT` executa oito `T` operações, use o seguinte código C#:

```csharp 
// using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
// using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.UsePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tCountAll = sim.GetMetric<ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
double tCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
```

A primeira parte do programa é executada `ApplySampleWithCCNOT` . A segunda parte usa o [`QCTraceSimulator.GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) método para recuperar o número de `T` operações executadas por `ApplySampleWithCCNOT` : 

Quando você chama `GetMetric` com dois parâmetros de tipo, ele retorna o valor da métrica associada a uma determinada borda de gráfico de chamada. No exemplo anterior, o programa chama a `Primitive.CCNOT` operação dentro `ApplySampleWithCCNOT` e, portanto, o grafo de chamada contém a borda `<Primitive.CCNOT, ApplySampleWithCCNOT>` . 

Para recuperar o número de `CNOT` operações usadas, adicione a seguinte linha:
```csharp
double cxCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.CX);
```

Por fim, você pode gerar todas as estatísticas coletadas pelo contador de operações primitivas no formato CSV usando o seguinte:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.primitiveOperationsCounter];
```

## <a name="see-also"></a>Confira também

- A visão geral do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro) do quantum do kit de desenvolvimento Quantum.
- A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> referência da API.
- A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> referência da API.
- A <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.PrimitiveOperationsGroupsNames> referência da API.