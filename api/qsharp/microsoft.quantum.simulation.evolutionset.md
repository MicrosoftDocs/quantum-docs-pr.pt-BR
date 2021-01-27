---
uid: Microsoft.Quantum.Simulation.EvolutionSet
title: Tipo definido pelo usuário do evolucionárioset
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EvolutionSet
qsharp.summary: >-
  Represents a set of gates that can be readily implemented and used to implement simulation algorithms.

  Elements in the set are indexed by a  <xref:microsoft.quantum.simulation.generatorindex>, and each set is described by a function from `GeneratorIndex` to  <xref:microsoft.quantum.simulation.evolutionunitary>, which are operations parameterized by a real number representing time
ms.openlocfilehash: 35c0b24da284a5871fd11b6d624102b853b89d19
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856064"
---
# <a name="evolutionset-user-defined-type"></a><span data-ttu-id="81d84-102">Tipo definido pelo usuário do evolucionárioset</span><span class="sxs-lookup"><span data-stu-id="81d84-102">EvolutionSet user defined type</span></span>

<span data-ttu-id="81d84-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="81d84-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="81d84-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="81d84-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="81d84-105">Representa um conjunto de Gates que podem ser prontamente implementados e usados para implementar algoritmos de simulação.</span><span class="sxs-lookup"><span data-stu-id="81d84-105">Represents a set of gates that can be readily implemented and used to implement simulation algorithms.</span></span>

<span data-ttu-id="81d84-106">Os elementos no conjunto são indexados por um  <xref:microsoft.quantum.simulation.generatorindex> , e cada conjunto é descrito por uma função de `GeneratorIndex` para  <xref:microsoft.quantum.simulation.evolutionunitary> , que são operações parametrizadas por um número real que representa a hora</span><span class="sxs-lookup"><span data-stu-id="81d84-106">Elements in the set are indexed by a  <xref:microsoft.quantum.simulation.generatorindex>, and each set is described by a function from `GeneratorIndex` to  <xref:microsoft.quantum.simulation.evolutionunitary>, which are operations parameterized by a real number representing time</span></span>

```qsharp

newtype EvolutionSet = ((Microsoft.Quantum.Simulation.GeneratorIndex -> Microsoft.Quantum.Simulation.EvolutionUnitary));
```

