---
uid: Microsoft.Quantum.Arrays.MappedByIndex
title: Função MappedByIndex
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedByIndex
qsharp.summary: Given an array and a function that is defined for the indexed elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 584cabcb7b6059ae5d311f13f5f75bd1f87bdba5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845659"
---
# <a name="mappedbyindex-function"></a><span data-ttu-id="d88bd-102">Função MappedByIndex</span><span class="sxs-lookup"><span data-stu-id="d88bd-102">MappedByIndex function</span></span>

<span data-ttu-id="d88bd-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="d88bd-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="d88bd-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d88bd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d88bd-105">Dada uma matriz e uma função que é definida para os elementos indexados da matriz, retorna uma nova matriz que consiste nas imagens da matriz original sob a função.</span><span class="sxs-lookup"><span data-stu-id="d88bd-105">Given an array and a function that is defined for the indexed elements of the array, returns a new array that consists of the images of the original array under the function.</span></span>

```qsharp
function MappedByIndex<'T, 'U> (mapper : ((Int, 'T) -> 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a><span data-ttu-id="d88bd-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="d88bd-106">Input</span></span>

### <a name="mapper--intt---u"></a><span data-ttu-id="d88bd-107">mapeador: ([int](xref:microsoft.quantum.lang-ref.int), ' t)-> ' U</span><span class="sxs-lookup"><span data-stu-id="d88bd-107">mapper : ([Int](xref:microsoft.quantum.lang-ref.int),'T) -> 'U</span></span>

<span data-ttu-id="d88bd-108">Uma função de `(Int, 'T)` para `'U` que é usada para mapear elementos e seus índices.</span><span class="sxs-lookup"><span data-stu-id="d88bd-108">A function from `(Int, 'T)` to `'U` that is used to map elements and their indices.</span></span>


### <a name="array--t"></a><span data-ttu-id="d88bd-109">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="d88bd-109">array : 'T[]</span></span>

<span data-ttu-id="d88bd-110">Uma matriz de elementos `'T` .</span><span class="sxs-lookup"><span data-stu-id="d88bd-110">An array of elements over `'T`.</span></span>



## <a name="output--u"></a><span data-ttu-id="d88bd-111">Saída: ' U []</span><span class="sxs-lookup"><span data-stu-id="d88bd-111">Output : 'U[]</span></span>

<span data-ttu-id="d88bd-112">Uma matriz `'U[]` de elementos que são mapeados pela `mapper` função.</span><span class="sxs-lookup"><span data-stu-id="d88bd-112">An array `'U[]` of elements that are mapped by the `mapper` function.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d88bd-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="d88bd-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d88bd-114">T'</span><span class="sxs-lookup"><span data-stu-id="d88bd-114">'T</span></span>

<span data-ttu-id="d88bd-115">O tipo de `array` elementos.</span><span class="sxs-lookup"><span data-stu-id="d88bd-115">The type of `array` elements.</span></span>
### <a name="u"></a><span data-ttu-id="d88bd-116">' U</span><span class="sxs-lookup"><span data-stu-id="d88bd-116">'U</span></span>

<span data-ttu-id="d88bd-117">O tipo de resultado da `mapper` função.</span><span class="sxs-lookup"><span data-stu-id="d88bd-117">The result type of the `mapper` function.</span></span>

## <a name="example"></a><span data-ttu-id="d88bd-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d88bd-118">Example</span></span>

<span data-ttu-id="d88bd-119">As duas linhas a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="d88bd-119">The following two lines are equivalent:</span></span>

```qsharp
let arr = MapIndex(f, [x0, x1, x2]);
```

<span data-ttu-id="d88bd-120">e</span><span class="sxs-lookup"><span data-stu-id="d88bd-120">and</span></span>

```qsharp
let arr = [f(0, x0), f(1, x1), f(2, x2)];
```

## <a name="see-also"></a><span data-ttu-id="d88bd-121">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d88bd-121">See Also</span></span>

- [<span data-ttu-id="d88bd-122">Microsoft. Quantum. arrays. mapeado</span><span class="sxs-lookup"><span data-stu-id="d88bd-122">Microsoft.Quantum.Arrays.Mapped</span></span>](xref:Microsoft.Quantum.Arrays.Mapped)