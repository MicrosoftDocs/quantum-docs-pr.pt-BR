---
uid: Microsoft.Quantum.Arrays.Count
title: função Count
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Count
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, returns the number of elements an array that consists of those elements that satisfy the predicate.
ms.openlocfilehash: e178ee63526e3485e8cc83a3ba8f827d8ecac552
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842845"
---
# <a name="count-function"></a><span data-ttu-id="ed9f9-102">função Count</span><span class="sxs-lookup"><span data-stu-id="ed9f9-102">Count function</span></span>

<span data-ttu-id="ed9f9-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="ed9f9-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="ed9f9-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ed9f9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ed9f9-105">Dada uma matriz e um predicado que é definido para os elementos da matriz, retorna o número de elementos que uma matriz consiste nesses elementos que atendem ao predicado.</span><span class="sxs-lookup"><span data-stu-id="ed9f9-105">Given an array and a predicate that is defined for the elements of the array, returns the number of elements an array that consists of those elements that satisfy the predicate.</span></span>

```qsharp
function Count<'T> (predicate : ('T -> Bool), array : 'T[]) : Int
```


## <a name="input"></a><span data-ttu-id="ed9f9-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="ed9f9-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="ed9f9-107">predicado: [booliano](xref:microsoft.quantum.lang-ref.bool) -> bool</span><span class="sxs-lookup"><span data-stu-id="ed9f9-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="ed9f9-108">Uma função de `'T` para booliano que é usada para filtrar elementos.</span><span class="sxs-lookup"><span data-stu-id="ed9f9-108">A function from `'T` to Boolean that is used to filter elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="ed9f9-109">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="ed9f9-109">array : 'T[]</span></span>

<span data-ttu-id="ed9f9-110">Uma matriz de elementos `'T` .</span><span class="sxs-lookup"><span data-stu-id="ed9f9-110">An array of elements over `'T`.</span></span>



## <a name="output--int"></a><span data-ttu-id="ed9f9-111">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ed9f9-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ed9f9-112">O número de elementos no `array` que atendem ao predicado.</span><span class="sxs-lookup"><span data-stu-id="ed9f9-112">The number of elements in `array` that satisfy the predicate.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ed9f9-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="ed9f9-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ed9f9-114">T'</span><span class="sxs-lookup"><span data-stu-id="ed9f9-114">'T</span></span>

<span data-ttu-id="ed9f9-115">O tipo de `array` elementos.</span><span class="sxs-lookup"><span data-stu-id="ed9f9-115">The type of `array` elements.</span></span>

## <a name="example"></a><span data-ttu-id="ed9f9-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ed9f9-116">Example</span></span>

<span data-ttu-id="ed9f9-117">O código a seguir demonstra a função "Count".</span><span class="sxs-lookup"><span data-stu-id="ed9f9-117">The following code demonstrates the "Count" function.</span></span>
<span data-ttu-id="ed9f9-118">Um predicado é definido usando a @"microsoft.quantum.logical.greaterthani" função:</span><span class="sxs-lookup"><span data-stu-id="ed9f9-118">A predicate is defined using the @"microsoft.quantum.logical.greaterthani" function:</span></span>

```qsharp
 let predicate = GreaterThanI(_, 5);
 let count = Count(predicate, [2, 5, 9, 1, 8]);
 // count = 2
```

## <a name="remarks"></a><span data-ttu-id="ed9f9-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed9f9-119">Remarks</span></span>

<span data-ttu-id="ed9f9-120">A função é definida para tipos genéricos, ou seja, sempre que temos uma matriz `'T[]` e um predicado, `'T -> Bool` podemos filtrar elementos.</span><span class="sxs-lookup"><span data-stu-id="ed9f9-120">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a predicate `'T -> Bool` we can filter elements.</span></span>