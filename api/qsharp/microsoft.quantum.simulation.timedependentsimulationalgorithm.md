---
uid: Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm
title: Tipo definido pelo usuário TimeDependentSimulationAlgorithm
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentSimulationAlgorithm
qsharp.summary: >-
  Represents a time-dependent simulation algorithm.

  A time-dependent simulation technique converts an <xref:microsoft.quantum.simulation.evolutionschedule> to unitary time-evolution for some time-interval.
ms.openlocfilehash: b495a9fd96c78872f84e8f8183105f6290f70655
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192512"
---
# <a name="timedependentsimulationalgorithm-user-defined-type"></a>Tipo definido pelo usuário TimeDependentSimulationAlgorithm

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Representa um algoritmo de simulação dependente de tempo.

Uma técnica de simulação dependente de tempo converte um <xref:microsoft.quantum.simulation.evolutionschedule>
para o tempo de evolução unitário de um intervalo de tempo.

```qsharp

newtype TimeDependentSimulationAlgorithm = (((Double, Microsoft.Quantum.Simulation.EvolutionSchedule, Qubit[]) => Unit is Adj + Ctl));
```

