---
uid: Microsoft.Quantum.Arrays.MappedByIndex
title: Função MappedByIndex
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedByIndex
qsharp.summary: Given an array and a function that is defined for the indexed elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 07ca523248c363f2229551a14e77803dc4f4f82e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694440"
---
# <a name="mappedbyindex-function"></a><span data-ttu-id="08929-102">Função MappedByIndex</span><span class="sxs-lookup"><span data-stu-id="08929-102">MappedByIndex function</span></span>

<span data-ttu-id="08929-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="08929-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="08929-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="08929-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="08929-105">Dada uma matriz e uma função que é definida para os elementos indexados da matriz, retorna uma nova matriz que consiste nas imagens da matriz original sob a função.</span><span class="sxs-lookup"><span data-stu-id="08929-105">Given an array and a function that is defined for the indexed elements of the array, returns a new array that consists of the images of the original array under the function.</span></span>

```qsharp
function MappedByIndex<'T, 'U> (mapper : ((Int, 'T) -> 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a><span data-ttu-id="08929-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="08929-106">Input</span></span>

### <a name="mapper--intt---u"></a><span data-ttu-id="08929-107">mapeador: ([int](xref:microsoft.quantum.lang-ref.int), ' t)-> ' U</span><span class="sxs-lookup"><span data-stu-id="08929-107">mapper : ([Int](xref:microsoft.quantum.lang-ref.int),'T) -> 'U</span></span>

<span data-ttu-id="08929-108">Uma função de `(Int, 'T)` para `'U` que é usada para mapear elementos e seus índices.</span><span class="sxs-lookup"><span data-stu-id="08929-108">A function from `(Int, 'T)` to `'U` that is used to map elements and their indices.</span></span>


### <a name="array--t"></a><span data-ttu-id="08929-109">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="08929-109">array : 'T[]</span></span>

<span data-ttu-id="08929-110">Uma matriz de elementos `'T` .</span><span class="sxs-lookup"><span data-stu-id="08929-110">An array of elements over `'T`.</span></span>



## <a name="output--u"></a><span data-ttu-id="08929-111">Saída: ' U []</span><span class="sxs-lookup"><span data-stu-id="08929-111">Output : 'U[]</span></span>

<span data-ttu-id="08929-112">Uma matriz `'U[]` de elementos que são mapeados pela `mapper` função.</span><span class="sxs-lookup"><span data-stu-id="08929-112">An array `'U[]` of elements that are mapped by the `mapper` function.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="08929-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="08929-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="08929-114">T'</span><span class="sxs-lookup"><span data-stu-id="08929-114">'T</span></span>

<span data-ttu-id="08929-115">O tipo de `array` elementos.</span><span class="sxs-lookup"><span data-stu-id="08929-115">The type of `array` elements.</span></span>
### <a name="u"></a><span data-ttu-id="08929-116">' U</span><span class="sxs-lookup"><span data-stu-id="08929-116">'U</span></span>

<span data-ttu-id="08929-117">O tipo de resultado da `mapper` função.</span><span class="sxs-lookup"><span data-stu-id="08929-117">The result type of the `mapper` function.</span></span>

## <a name="see-also"></a><span data-ttu-id="08929-118">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="08929-118">See Also</span></span>

- [<span data-ttu-id="08929-119">Microsoft. Quantum. arrays. mapeado</span><span class="sxs-lookup"><span data-stu-id="08929-119">Microsoft.Quantum.Arrays.Mapped</span></span>](xref:Microsoft.Quantum.Arrays.Mapped)