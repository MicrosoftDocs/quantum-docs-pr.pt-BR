---
uid: Microsoft.Quantum.Simulation.PauliEvolutionSet
title: Função PauliEvolutionSet
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliEvolutionSet
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.
ms.openlocfilehash: fb53b90b6ab5ce1003f66b68a8c2ad8b3631f627
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230337"
---
# <a name="paulievolutionset-function"></a><span data-ttu-id="3adda-102">Função PauliEvolutionSet</span><span class="sxs-lookup"><span data-stu-id="3adda-102">PauliEvolutionSet function</span></span>

<span data-ttu-id="3adda-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="3adda-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="3adda-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3adda-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3adda-105">Representa um gerador dinâmico como um conjunto de Gates e uma expansão na base Pauli.</span><span class="sxs-lookup"><span data-stu-id="3adda-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.</span></span>

```qsharp
function PauliEvolutionSet () : Microsoft.Quantum.Simulation.EvolutionSet
```


## <a name="output--evolutionset"></a><span data-ttu-id="3adda-106">Saída: [evolucionárioset](xref:Microsoft.Quantum.Simulation.EvolutionSet)</span><span class="sxs-lookup"><span data-stu-id="3adda-106">Output : [EvolutionSet](xref:Microsoft.Quantum.Simulation.EvolutionSet)</span></span>

<span data-ttu-id="3adda-107">Um `EvolutionSet` que mapeia um `GeneratorIndex` para a base Pauli para um ' EvolutionUnitary.</span><span class="sxs-lookup"><span data-stu-id="3adda-107">An `EvolutionSet` that maps a `GeneratorIndex` for the Pauli basis to an \`EvolutionUnitary.</span></span>

## <a name="remarks"></a><span data-ttu-id="3adda-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="3adda-108">Remarks</span></span>

<span data-ttu-id="3adda-109">Isso é obtido pela aplicação parcial do <xref:microsoft.quantum.simulation.paulievolutionfunction> .</span><span class="sxs-lookup"><span data-stu-id="3adda-109">This is obtained by partial application of <xref:microsoft.quantum.simulation.paulievolutionfunction>.</span></span>