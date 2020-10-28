---
uid: Microsoft.Quantum.Simulation.EvolutionSet
title: Tipo definido pelo usuário do evolucionárioset
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EvolutionSet
qsharp.summary: >-
  Represents a set of gates that can be readily implemented and used to implement simulation algorithms.

  Elements in the set are indexed by a  <xref:microsoft.quantum.simulation.generatorindex>, and each set is described by a function from `GeneratorIndex` to  <xref:microsoft.quantum.simulation.evolutionunitary>, which are operations parameterized by a real number representing time
ms.openlocfilehash: 41504837b281b1021a2d09ef75acc10315b4fd07
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693214"
---
# <a name="evolutionset-user-defined-type"></a><span data-ttu-id="fe8fb-102">Tipo definido pelo usuário do evolucionárioset</span><span class="sxs-lookup"><span data-stu-id="fe8fb-102">EvolutionSet user defined type</span></span>

<span data-ttu-id="fe8fb-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="fe8fb-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="fe8fb-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="fe8fb-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="fe8fb-105">Representa um conjunto de Gates que podem ser prontamente implementados e usados para implementar algoritmos de simulação.</span><span class="sxs-lookup"><span data-stu-id="fe8fb-105">Represents a set of gates that can be readily implemented and used to implement simulation algorithms.</span></span>

<span data-ttu-id="fe8fb-106">Os elementos no conjunto são indexados por um  <xref:microsoft.quantum.simulation.generatorindex> , e cada conjunto é descrito por uma função de `GeneratorIndex` para  <xref:microsoft.quantum.simulation.evolutionunitary> , que são operações parametrizadas por um número real que representa a hora</span><span class="sxs-lookup"><span data-stu-id="fe8fb-106">Elements in the set are indexed by a  <xref:microsoft.quantum.simulation.generatorindex>, and each set is described by a function from `GeneratorIndex` to  <xref:microsoft.quantum.simulation.evolutionunitary>, which are operations parameterized by a real number representing time</span></span>

```qsharp

newtype EvolutionSet = ((Microsoft.Quantum.Simulation.GeneratorIndex -> Microsoft.Quantum.Simulation.EvolutionUnitary));
```

