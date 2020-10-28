---
uid: Microsoft.Quantum.Arrays.ElementsAt
title: Função ElementsAt
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ElementsAt
qsharp.summary: Returns the array's elements at a given range of indices.
ms.openlocfilehash: b4bbba4dc83c4f9b89cdcb8ec32769f1c586357e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694488"
---
# <a name="elementsat-function"></a><span data-ttu-id="e26d1-102">Função ElementsAt</span><span class="sxs-lookup"><span data-stu-id="e26d1-102">ElementsAt function</span></span>

<span data-ttu-id="e26d1-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="e26d1-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="e26d1-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e26d1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e26d1-105">Retorna os elementos da matriz em um determinado intervalo de índices.</span><span class="sxs-lookup"><span data-stu-id="e26d1-105">Returns the array's elements at a given range of indices.</span></span>

```qsharp
function ElementsAt<'T> (range : Range, array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="e26d1-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="e26d1-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="e26d1-107">intervalo: [intervalo](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="e26d1-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="e26d1-108">Intervalo de índices de matriz</span><span class="sxs-lookup"><span data-stu-id="e26d1-108">Range of array indexes</span></span>


### <a name="array--t"></a><span data-ttu-id="e26d1-109">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="e26d1-109">array : 'T[]</span></span>

<span data-ttu-id="e26d1-110">Array</span><span class="sxs-lookup"><span data-stu-id="e26d1-110">Array</span></span>



## <a name="output--t"></a><span data-ttu-id="e26d1-111">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="e26d1-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e26d1-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="e26d1-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e26d1-113">T'</span><span class="sxs-lookup"><span data-stu-id="e26d1-113">'T</span></span>

<span data-ttu-id="e26d1-114">O tipo de cada elemento de `array` .</span><span class="sxs-lookup"><span data-stu-id="e26d1-114">The type of each element of `array`.</span></span>

## <a name="see-also"></a><span data-ttu-id="e26d1-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e26d1-115">See Also</span></span>

- [<span data-ttu-id="e26d1-116">Microsoft. Quantum. arrays. ElementAt</span><span class="sxs-lookup"><span data-stu-id="e26d1-116">Microsoft.Quantum.Arrays.ElementAt</span></span>](xref:Microsoft.Quantum.Arrays.ElementAt)
- [<span data-ttu-id="e26d1-117">Microsoft. Quantum. arrays. LookupFunction</span><span class="sxs-lookup"><span data-stu-id="e26d1-117">Microsoft.Quantum.Arrays.LookupFunction</span></span>](xref:Microsoft.Quantum.Arrays.LookupFunction)