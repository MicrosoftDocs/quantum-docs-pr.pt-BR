---
uid: Microsoft.Quantum.Arrays.MappedOverRange
title: Função MappedOverRange
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedOverRange
qsharp.summary: Given a range and a function that takes an integer as input, returns a new array that consists of the images of the range values under the function.
ms.openlocfilehash: e527a3ca1fd7571836f4f79bb453581f53d1db2b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694438"
---
# <a name="mappedoverrange-function"></a><span data-ttu-id="ec580-102">Função MappedOverRange</span><span class="sxs-lookup"><span data-stu-id="ec580-102">MappedOverRange function</span></span>

<span data-ttu-id="ec580-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="ec580-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="ec580-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ec580-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ec580-105">Dado um intervalo e uma função que usa um inteiro como entrada, retorna uma nova matriz que consiste nas imagens dos valores de intervalo na função.</span><span class="sxs-lookup"><span data-stu-id="ec580-105">Given a range and a function that takes an integer as input, returns a new array that consists of the images of the range values under the function.</span></span>

```qsharp
function MappedOverRange<'T> (mapper : (Int -> 'T), range : Range) : 'T[]
```


## <a name="input"></a><span data-ttu-id="ec580-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="ec580-106">Input</span></span>

### <a name="mapper--int---t"></a><span data-ttu-id="ec580-107">mapeador: [int](xref:microsoft.quantum.lang-ref.int) -> ' t</span><span class="sxs-lookup"><span data-stu-id="ec580-107">mapper : [Int](xref:microsoft.quantum.lang-ref.int) -> 'T</span></span>

<span data-ttu-id="ec580-108">Uma função de `Int` para `'T` que é usada para mapear valores de intervalo.</span><span class="sxs-lookup"><span data-stu-id="ec580-108">A function from `Int` to `'T` that is used to map range values.</span></span>


### <a name="range--range"></a><span data-ttu-id="ec580-109">intervalo: [intervalo](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="ec580-109">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="ec580-110">Um intervalo de inteiros.</span><span class="sxs-lookup"><span data-stu-id="ec580-110">A range of integers.</span></span>



## <a name="output--t"></a><span data-ttu-id="ec580-111">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="ec580-111">Output : 'T[]</span></span>

<span data-ttu-id="ec580-112">Uma matriz `'T[]` de elementos que são mapeados pela `mapper` função.</span><span class="sxs-lookup"><span data-stu-id="ec580-112">An array `'T[]` of elements that are mapped by the `mapper` function.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ec580-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="ec580-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ec580-114">T'</span><span class="sxs-lookup"><span data-stu-id="ec580-114">'T</span></span>

<span data-ttu-id="ec580-115">O tipo de resultado da `mapper` função.</span><span class="sxs-lookup"><span data-stu-id="ec580-115">The result type of the `mapper` function.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec580-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec580-116">Remarks</span></span>

<span data-ttu-id="ec580-117">A função é definida para tipos genéricos, ou seja, sempre que temos uma função, `mapper: Int -> 'T` podemos mapear os valores do intervalo e produzir uma matriz do tipo `'T[]` .</span><span class="sxs-lookup"><span data-stu-id="ec580-117">The function is defined for generic types, i.e., whenever we have a function `mapper: Int -> 'T` we can map the values of the range and produce an array of type `'T[]`.</span></span>

## <a name="see-also"></a><span data-ttu-id="ec580-118">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ec580-118">See Also</span></span>

- [<span data-ttu-id="ec580-119">Microsoft. Quantum. arrays. mapeado</span><span class="sxs-lookup"><span data-stu-id="ec580-119">Microsoft.Quantum.Arrays.Mapped</span></span>](xref:Microsoft.Quantum.Arrays.Mapped)