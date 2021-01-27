---
uid: Microsoft.Quantum.Arrays.MappedOverRange
title: Função MappedOverRange
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedOverRange
qsharp.summary: Given a range and a function that takes an integer as input, returns a new array that consists of the images of the range values under the function.
ms.openlocfilehash: 7093043e2a290e6132774b8fe154d3627a254f27
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845646"
---
# <a name="mappedoverrange-function"></a><span data-ttu-id="8d7ae-102">Função MappedOverRange</span><span class="sxs-lookup"><span data-stu-id="8d7ae-102">MappedOverRange function</span></span>

<span data-ttu-id="8d7ae-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="8d7ae-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="8d7ae-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8d7ae-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8d7ae-105">Dado um intervalo e uma função que usa um inteiro como entrada, retorna uma nova matriz que consiste nas imagens dos valores de intervalo na função.</span><span class="sxs-lookup"><span data-stu-id="8d7ae-105">Given a range and a function that takes an integer as input, returns a new array that consists of the images of the range values under the function.</span></span>

```qsharp
function MappedOverRange<'T> (mapper : (Int -> 'T), range : Range) : 'T[]
```


## <a name="input"></a><span data-ttu-id="8d7ae-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="8d7ae-106">Input</span></span>

### <a name="mapper--int---t"></a><span data-ttu-id="8d7ae-107">mapeador: [int](xref:microsoft.quantum.lang-ref.int) -> ' t</span><span class="sxs-lookup"><span data-stu-id="8d7ae-107">mapper : [Int](xref:microsoft.quantum.lang-ref.int) -> 'T</span></span>

<span data-ttu-id="8d7ae-108">Uma função de `Int` para `'T` que é usada para mapear valores de intervalo.</span><span class="sxs-lookup"><span data-stu-id="8d7ae-108">A function from `Int` to `'T` that is used to map range values.</span></span>


### <a name="range--range"></a><span data-ttu-id="8d7ae-109">intervalo: [intervalo](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="8d7ae-109">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="8d7ae-110">Um intervalo de inteiros.</span><span class="sxs-lookup"><span data-stu-id="8d7ae-110">A range of integers.</span></span>



## <a name="output--t"></a><span data-ttu-id="8d7ae-111">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="8d7ae-111">Output : 'T[]</span></span>

<span data-ttu-id="8d7ae-112">Uma matriz `'T[]` de elementos que são mapeados pela `mapper` função.</span><span class="sxs-lookup"><span data-stu-id="8d7ae-112">An array `'T[]` of elements that are mapped by the `mapper` function.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="8d7ae-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="8d7ae-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8d7ae-114">T'</span><span class="sxs-lookup"><span data-stu-id="8d7ae-114">'T</span></span>

<span data-ttu-id="8d7ae-115">O tipo de resultado da `mapper` função.</span><span class="sxs-lookup"><span data-stu-id="8d7ae-115">The result type of the `mapper` function.</span></span>

## <a name="example"></a><span data-ttu-id="8d7ae-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="8d7ae-116">Example</span></span>

<span data-ttu-id="8d7ae-117">Este exemplo adiciona 1 a um intervalo de números pares:</span><span class="sxs-lookup"><span data-stu-id="8d7ae-117">This example adds 1 to a range of even numbers:</span></span>

```qsharp
let numbers = MappedOverRange(PlusI(1, _), 0..2..10);
// numbers = [1, 3, 5, 7, 9, 11]
```

## <a name="remarks"></a><span data-ttu-id="8d7ae-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="8d7ae-118">Remarks</span></span>

<span data-ttu-id="8d7ae-119">A função é definida para tipos genéricos, ou seja, sempre que temos uma função, `mapper: Int -> 'T` podemos mapear os valores do intervalo e produzir uma matriz do tipo `'T[]` .</span><span class="sxs-lookup"><span data-stu-id="8d7ae-119">The function is defined for generic types, i.e., whenever we have a function `mapper: Int -> 'T` we can map the values of the range and produce an array of type `'T[]`.</span></span>

## <a name="see-also"></a><span data-ttu-id="8d7ae-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="8d7ae-120">See Also</span></span>

- [<span data-ttu-id="8d7ae-121">Microsoft. Quantum. arrays. mapeado</span><span class="sxs-lookup"><span data-stu-id="8d7ae-121">Microsoft.Quantum.Arrays.Mapped</span></span>](xref:Microsoft.Quantum.Arrays.Mapped)