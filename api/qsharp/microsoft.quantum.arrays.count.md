---
uid: Microsoft.Quantum.Arrays.Count
title: função Count
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Count
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, returns the number of elements an array that consists of those elements that satisfy the predicate.
ms.openlocfilehash: 48b75cc6d6584f899223a0803f31fd174836f303
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221548"
---
# <a name="count-function"></a><span data-ttu-id="e757f-102">função Count</span><span class="sxs-lookup"><span data-stu-id="e757f-102">Count function</span></span>

<span data-ttu-id="e757f-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="e757f-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="e757f-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e757f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e757f-105">Dada uma matriz e um predicado que é definido para os elementos da matriz, retorna o número de elementos que uma matriz consiste nesses elementos que atendem ao predicado.</span><span class="sxs-lookup"><span data-stu-id="e757f-105">Given an array and a predicate that is defined for the elements of the array, returns the number of elements an array that consists of those elements that satisfy the predicate.</span></span>

```qsharp
function Count<'T> (predicate : ('T -> Bool), array : 'T[]) : Int
```


## <a name="input"></a><span data-ttu-id="e757f-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="e757f-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="e757f-107">predicado: [booliano](xref:microsoft.quantum.lang-ref.bool) -> bool</span><span class="sxs-lookup"><span data-stu-id="e757f-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="e757f-108">Uma função de `'T` para booliano que é usada para filtrar elementos.</span><span class="sxs-lookup"><span data-stu-id="e757f-108">A function from `'T` to Boolean that is used to filter elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="e757f-109">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="e757f-109">array : 'T[]</span></span>

<span data-ttu-id="e757f-110">Uma matriz de elementos `'T` .</span><span class="sxs-lookup"><span data-stu-id="e757f-110">An array of elements over `'T`.</span></span>



## <a name="output--int"></a><span data-ttu-id="e757f-111">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e757f-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e757f-112">O número de elementos no `array` que atendem ao predicado.</span><span class="sxs-lookup"><span data-stu-id="e757f-112">The number of elements in `array` that satisfy the predicate.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="e757f-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="e757f-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e757f-114">T'</span><span class="sxs-lookup"><span data-stu-id="e757f-114">'T</span></span>

<span data-ttu-id="e757f-115">O tipo de `array` elementos.</span><span class="sxs-lookup"><span data-stu-id="e757f-115">The type of `array` elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="e757f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e757f-116">Remarks</span></span>

<span data-ttu-id="e757f-117">A função é definida para tipos genéricos, ou seja, sempre que temos uma matriz `'T[]` e um predicado, `'T -> Bool` podemos filtrar elementos.</span><span class="sxs-lookup"><span data-stu-id="e757f-117">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a predicate `'T -> Bool` we can filter elements.</span></span>