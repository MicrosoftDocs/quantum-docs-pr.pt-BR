---
uid: Microsoft.Quantum.Simulation.SimulationAlgorithm
title: Tipo definido pelo usuário SimulationAlgorithm
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: SimulationAlgorithm
qsharp.summary: >-
  Represents a time-independent simulation algorithm.

  A time-independent simulation technique converts an <xref:microsoft.quantum.simulation.evolutiongenerator> to unitary time evolution for some time-interval.
ms.openlocfilehash: d7b233ee76d79072f59ecfd001245848cb780eec
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851037"
---
# <a name="simulationalgorithm-user-defined-type"></a><span data-ttu-id="e5979-102">Tipo definido pelo usuário SimulationAlgorithm</span><span class="sxs-lookup"><span data-stu-id="e5979-102">SimulationAlgorithm user defined type</span></span>

<span data-ttu-id="e5979-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="e5979-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="e5979-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e5979-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e5979-105">Representa um algoritmo de simulação independente de tempo.</span><span class="sxs-lookup"><span data-stu-id="e5979-105">Represents a time-independent simulation algorithm.</span></span>

<span data-ttu-id="e5979-106">Uma técnica de simulação independente de tempo converte um <xref:microsoft.quantum.simulation.evolutiongenerator></span><span class="sxs-lookup"><span data-stu-id="e5979-106">A time-independent simulation technique converts an <xref:microsoft.quantum.simulation.evolutiongenerator></span></span>
<span data-ttu-id="e5979-107">para a evolução de tempo unitário para um intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="e5979-107">to unitary time evolution for some time-interval.</span></span>

```qsharp

newtype SimulationAlgorithm = (((Double, Microsoft.Quantum.Simulation.EvolutionGenerator, Qubit[]) => Unit is Adj + Ctl));
```

