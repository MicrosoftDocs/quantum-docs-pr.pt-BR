---
uid: Microsoft.Quantum.Simulation.PauliEvolutionSet
title: Função PauliEvolutionSet
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliEvolutionSet
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.
ms.openlocfilehash: 89c81aca4cfad6087d764ac8f5a0f1426e905e4b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694931"
---
# <a name="paulievolutionset-function"></a><span data-ttu-id="39ccc-102">Função PauliEvolutionSet</span><span class="sxs-lookup"><span data-stu-id="39ccc-102">PauliEvolutionSet function</span></span>

<span data-ttu-id="39ccc-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="39ccc-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="39ccc-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="39ccc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="39ccc-105">Representa um gerador dinâmico como um conjunto de Gates e uma expansão na base Pauli.</span><span class="sxs-lookup"><span data-stu-id="39ccc-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.</span></span>

```qsharp
function PauliEvolutionSet () : Microsoft.Quantum.Simulation.EvolutionSet
```


## <a name="output--evolutionset"></a><span data-ttu-id="39ccc-106">Saída: [evolucionárioset](xref:Microsoft.Quantum.Simulation.EvolutionSet)</span><span class="sxs-lookup"><span data-stu-id="39ccc-106">Output : [EvolutionSet](xref:Microsoft.Quantum.Simulation.EvolutionSet)</span></span>

<span data-ttu-id="39ccc-107">Um `EvolutionSet` que mapeia um `GeneratorIndex` para a base Pauli para um ' EvolutionUnitary.</span><span class="sxs-lookup"><span data-stu-id="39ccc-107">An `EvolutionSet` that maps a `GeneratorIndex` for the Pauli basis to an \`EvolutionUnitary.</span></span>

## <a name="remarks"></a><span data-ttu-id="39ccc-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="39ccc-108">Remarks</span></span>

<span data-ttu-id="39ccc-109">Isso é obtido pela aplicação parcial do <xref:microsoft.quantum.simulation.paulievolutionfunction> .</span><span class="sxs-lookup"><span data-stu-id="39ccc-109">This is obtained by partial application of <xref:microsoft.quantum.simulation.paulievolutionfunction>.</span></span>