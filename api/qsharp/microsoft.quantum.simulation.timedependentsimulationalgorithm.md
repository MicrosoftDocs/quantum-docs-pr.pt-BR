---
uid: Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm
title: Tipo definido pelo usuário TimeDependentSimulationAlgorithm
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentSimulationAlgorithm
qsharp.summary: >-
  Represents a time-dependent simulation algorithm.

  A time-dependent simulation technique converts an <xref:microsoft.quantum.simulation.evolutionschedule> to unitary time-evolution for some time-interval.
ms.openlocfilehash: 9d2a1a853005495b5a9df60ac1f0dcbfbdf7637f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92697130"
---
# <a name="timedependentsimulationalgorithm-user-defined-type"></a><span data-ttu-id="0dddb-102">Tipo definido pelo usuário TimeDependentSimulationAlgorithm</span><span class="sxs-lookup"><span data-stu-id="0dddb-102">TimeDependentSimulationAlgorithm user defined type</span></span>

<span data-ttu-id="0dddb-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="0dddb-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="0dddb-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0dddb-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0dddb-105">Representa um algoritmo de simulação dependente de tempo.</span><span class="sxs-lookup"><span data-stu-id="0dddb-105">Represents a time-dependent simulation algorithm.</span></span>

<span data-ttu-id="0dddb-106">Uma técnica de simulação dependente de tempo converte um <xref:microsoft.quantum.simulation.evolutionschedule></span><span class="sxs-lookup"><span data-stu-id="0dddb-106">A time-dependent simulation technique converts an <xref:microsoft.quantum.simulation.evolutionschedule></span></span>
<span data-ttu-id="0dddb-107">para o tempo de evolução unitário de um intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="0dddb-107">to unitary time-evolution for some time-interval.</span></span>

```qsharp

newtype TimeDependentSimulationAlgorithm = (((Double, Microsoft.Quantum.Simulation.EvolutionSchedule, Qubit[]) => Unit is Adj + Ctl));
```

