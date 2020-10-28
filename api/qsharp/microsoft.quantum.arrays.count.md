---
uid: Microsoft.Quantum.Arrays.Count
title: função Count
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Count
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, returns the number of elements an array that consists of those elements that satisfy the predicate.
ms.openlocfilehash: 408a4a42dda6a4827db6d5865e2b4b8a8df5b37a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694498"
---
# <a name="count-function"></a><span data-ttu-id="bd5a6-102">função Count</span><span class="sxs-lookup"><span data-stu-id="bd5a6-102">Count function</span></span>

<span data-ttu-id="bd5a6-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="bd5a6-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="bd5a6-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bd5a6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bd5a6-105">Dada uma matriz e um predicado que é definido para os elementos da matriz, retorna o número de elementos que uma matriz consiste nesses elementos que atendem ao predicado.</span><span class="sxs-lookup"><span data-stu-id="bd5a6-105">Given an array and a predicate that is defined for the elements of the array, returns the number of elements an array that consists of those elements that satisfy the predicate.</span></span>

```qsharp
function Count<'T> (predicate : ('T -> Bool), array : 'T[]) : Int
```


## <a name="input"></a><span data-ttu-id="bd5a6-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="bd5a6-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="bd5a6-107">predicado: [booliano](xref:microsoft.quantum.lang-ref.bool) -> bool</span><span class="sxs-lookup"><span data-stu-id="bd5a6-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="bd5a6-108">Uma função de `'T` para booliano que é usada para filtrar elementos.</span><span class="sxs-lookup"><span data-stu-id="bd5a6-108">A function from `'T` to Boolean that is used to filter elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="bd5a6-109">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="bd5a6-109">array : 'T[]</span></span>

<span data-ttu-id="bd5a6-110">Uma matriz de elementos `'T` .</span><span class="sxs-lookup"><span data-stu-id="bd5a6-110">An array of elements over `'T`.</span></span>



## <a name="output--int"></a><span data-ttu-id="bd5a6-111">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bd5a6-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bd5a6-112">O número de elementos no `array` que atendem ao predicado.</span><span class="sxs-lookup"><span data-stu-id="bd5a6-112">The number of elements in `array` that satisfy the predicate.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="bd5a6-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="bd5a6-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="bd5a6-114">T'</span><span class="sxs-lookup"><span data-stu-id="bd5a6-114">'T</span></span>

<span data-ttu-id="bd5a6-115">O tipo de `array` elementos.</span><span class="sxs-lookup"><span data-stu-id="bd5a6-115">The type of `array` elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd5a6-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd5a6-116">Remarks</span></span>

<span data-ttu-id="bd5a6-117">A função é definida para tipos genéricos, ou seja, sempre que temos uma matriz `'T[]` e um predicado, `'T -> Bool` podemos filtrar elementos.</span><span class="sxs-lookup"><span data-stu-id="bd5a6-117">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a predicate `'T -> Bool` we can filter elements.</span></span>