---
uid: Microsoft.Quantum.Simulation.EvolutionGenerator
title: Tipo definido pelo usuário EvolutionGenerator
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EvolutionGenerator
qsharp.summary: >-
  Represents a dynamical generator as a set of simulatable gates and an expansion in terms of that basis.

  Last parameter for number of terms.
ms.openlocfilehash: 9e0fc5a232070c238aad943ab73f064999237c15
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229436"
---
# <a name="evolutiongenerator-user-defined-type"></a><span data-ttu-id="9b9fd-102">Tipo definido pelo usuário EvolutionGenerator</span><span class="sxs-lookup"><span data-stu-id="9b9fd-102">EvolutionGenerator user defined type</span></span>

<span data-ttu-id="9b9fd-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="9b9fd-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="9b9fd-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9b9fd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9b9fd-105">Representa um gerador dinâmico como um conjunto de Gates simulable e uma expansão em termos de base.</span><span class="sxs-lookup"><span data-stu-id="9b9fd-105">Represents a dynamical generator as a set of simulatable gates and an expansion in terms of that basis.</span></span>

<span data-ttu-id="9b9fd-106">Último parâmetro para o número de termos.</span><span class="sxs-lookup"><span data-stu-id="9b9fd-106">Last parameter for number of terms.</span></span>

```qsharp

newtype EvolutionGenerator = (Microsoft.Quantum.Simulation.EvolutionSet, Microsoft.Quantum.Simulation.GeneratorSystem);
```

