---
uid: Microsoft.Quantum.Simulation.EvolutionSet
title: Tipo definido pelo usuário do evolucionárioset
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EvolutionSet
qsharp.summary: >-
  Represents a set of gates that can be readily implemented and used to implement simulation algorithms.

  Elements in the set are indexed by a  <xref:microsoft.quantum.simulation.generatorindex>, and each set is described by a function from `GeneratorIndex` to  <xref:microsoft.quantum.simulation.evolutionunitary>, which are operations parameterized by a real number representing time
ms.openlocfilehash: ee8f3c0716f035dcb0c4fad557092fbf8dd3c356
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229402"
---
# <a name="evolutionset-user-defined-type"></a><span data-ttu-id="73e44-102">Tipo definido pelo usuário do evolucionárioset</span><span class="sxs-lookup"><span data-stu-id="73e44-102">EvolutionSet user defined type</span></span>

<span data-ttu-id="73e44-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="73e44-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="73e44-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="73e44-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="73e44-105">Representa um conjunto de Gates que podem ser prontamente implementados e usados para implementar algoritmos de simulação.</span><span class="sxs-lookup"><span data-stu-id="73e44-105">Represents a set of gates that can be readily implemented and used to implement simulation algorithms.</span></span>

<span data-ttu-id="73e44-106">Os elementos no conjunto são indexados por um  <xref:microsoft.quantum.simulation.generatorindex> , e cada conjunto é descrito por uma função de `GeneratorIndex` para  <xref:microsoft.quantum.simulation.evolutionunitary> , que são operações parametrizadas por um número real que representa a hora</span><span class="sxs-lookup"><span data-stu-id="73e44-106">Elements in the set are indexed by a  <xref:microsoft.quantum.simulation.generatorindex>, and each set is described by a function from `GeneratorIndex` to  <xref:microsoft.quantum.simulation.evolutionunitary>, which are operations parameterized by a real number representing time</span></span>

```qsharp

newtype EvolutionSet = ((Microsoft.Quantum.Simulation.GeneratorIndex -> Microsoft.Quantum.Simulation.EvolutionUnitary));
```

