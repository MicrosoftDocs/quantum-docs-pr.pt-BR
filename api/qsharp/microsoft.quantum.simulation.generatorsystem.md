---
uid: Microsoft.Quantum.Simulation.GeneratorSystem
title: Tipo definido pelo usuário GeneratorSystem
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GeneratorSystem
qsharp.summary: >-
  Represents a collection of `GeneratorIndex`es.

  We iterate over this collection using a single-index integer, and the size of the collection is assumed to be known.
ms.openlocfilehash: c03caf99b197410c7fa15021c8acaaf55a728781
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696960"
---
# <a name="generatorsystem-user-defined-type"></a><span data-ttu-id="f6368-102">Tipo definido pelo usuário GeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="f6368-102">GeneratorSystem user defined type</span></span>

<span data-ttu-id="f6368-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="f6368-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="f6368-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f6368-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f6368-105">Representa uma coleção de `GeneratorIndex` es.</span><span class="sxs-lookup"><span data-stu-id="f6368-105">Represents a collection of `GeneratorIndex`es.</span></span>

<span data-ttu-id="f6368-106">Iteramos essa coleção usando um inteiro de índice único e o tamanho da coleção é considerado conhecido.</span><span class="sxs-lookup"><span data-stu-id="f6368-106">We iterate over this collection using a single-index integer, and the size of the collection is assumed to be known.</span></span>

```qsharp

newtype GeneratorSystem = (Int, (Int -> Microsoft.Quantum.Simulation.GeneratorIndex));
```



## <a name="remarks"></a><span data-ttu-id="f6368-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6368-107">Remarks</span></span>

<span data-ttu-id="f6368-108">As instâncias do `GeneratorSystem` podem ser definidas facilmente usando a <xref:microsoft.quantum.arrays.lookupfunction> função.</span><span class="sxs-lookup"><span data-stu-id="f6368-108">Instances of `GeneratorSystem` can be defined easily using the <xref:microsoft.quantum.arrays.lookupfunction> function.</span></span>

## <a name="see-also"></a><span data-ttu-id="f6368-109">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="f6368-109">See Also</span></span>

- [<span data-ttu-id="f6368-110">Microsoft. Quantum. arrays. LookupFunction</span><span class="sxs-lookup"><span data-stu-id="f6368-110">Microsoft.Quantum.Arrays.LookupFunction</span></span>](xref:Microsoft.Quantum.Arrays.LookupFunction)