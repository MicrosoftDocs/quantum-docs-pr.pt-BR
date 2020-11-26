---
uid: Microsoft.Quantum.Simulation.GeneratorSystem
title: Tipo definido pelo usuário GeneratorSystem
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GeneratorSystem
qsharp.summary: >-
  Represents a collection of `GeneratorIndex`es.

  We iterate over this collection using a single-index integer, and the size of the collection is assumed to be known.
ms.openlocfilehash: 20092a8deca50c90f46f4d79c6b40b805f135754
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225220"
---
# <a name="generatorsystem-user-defined-type"></a><span data-ttu-id="0438b-102">Tipo definido pelo usuário GeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="0438b-102">GeneratorSystem user defined type</span></span>

<span data-ttu-id="0438b-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="0438b-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="0438b-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0438b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0438b-105">Representa uma coleção de `GeneratorIndex` es.</span><span class="sxs-lookup"><span data-stu-id="0438b-105">Represents a collection of `GeneratorIndex`es.</span></span>

<span data-ttu-id="0438b-106">Iteramos essa coleção usando um inteiro de índice único e o tamanho da coleção é considerado conhecido.</span><span class="sxs-lookup"><span data-stu-id="0438b-106">We iterate over this collection using a single-index integer, and the size of the collection is assumed to be known.</span></span>

```qsharp

newtype GeneratorSystem = (Int, (Int -> Microsoft.Quantum.Simulation.GeneratorIndex));
```



## <a name="remarks"></a><span data-ttu-id="0438b-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="0438b-107">Remarks</span></span>

<span data-ttu-id="0438b-108">As instâncias do `GeneratorSystem` podem ser definidas facilmente usando a <xref:microsoft.quantum.arrays.lookupfunction> função.</span><span class="sxs-lookup"><span data-stu-id="0438b-108">Instances of `GeneratorSystem` can be defined easily using the <xref:microsoft.quantum.arrays.lookupfunction> function.</span></span>

## <a name="see-also"></a><span data-ttu-id="0438b-109">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="0438b-109">See Also</span></span>

- [<span data-ttu-id="0438b-110">Microsoft. Quantum. arrays. LookupFunction</span><span class="sxs-lookup"><span data-stu-id="0438b-110">Microsoft.Quantum.Arrays.LookupFunction</span></span>](xref:Microsoft.Quantum.Arrays.LookupFunction)