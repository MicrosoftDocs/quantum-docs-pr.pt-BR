---
uid: Microsoft.Quantum.Arrays.Filtered
title: Função filtrada
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Filtered
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, returns an array that consists of those elements that satisfy the predicate.
ms.openlocfilehash: 4c786c69b0896b517f108611e32501867838aeb1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694476"
---
# <a name="filtered-function"></a><span data-ttu-id="aafd4-102">Função filtrada</span><span class="sxs-lookup"><span data-stu-id="aafd4-102">Filtered function</span></span>

<span data-ttu-id="aafd4-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="aafd4-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="aafd4-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="aafd4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="aafd4-105">Dada uma matriz e um predicado que é definido para os elementos da matriz, retorna uma matriz que consiste nesses elementos que atendem ao predicado.</span><span class="sxs-lookup"><span data-stu-id="aafd4-105">Given an array and a predicate that is defined for the elements of the array, returns an array that consists of those elements that satisfy the predicate.</span></span>

```qsharp
function Filtered<'T> (predicate : ('T -> Bool), array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="aafd4-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="aafd4-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="aafd4-107">predicado: [booliano](xref:microsoft.quantum.lang-ref.bool) -> bool</span><span class="sxs-lookup"><span data-stu-id="aafd4-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="aafd4-108">Uma função de `'T` para booliano que é usada para filtrar elementos.</span><span class="sxs-lookup"><span data-stu-id="aafd4-108">A function from `'T` to Boolean that is used to filter elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="aafd4-109">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="aafd4-109">array : 'T[]</span></span>

<span data-ttu-id="aafd4-110">Uma matriz de elementos `'T` .</span><span class="sxs-lookup"><span data-stu-id="aafd4-110">An array of elements over `'T`.</span></span>



## <a name="output--t"></a><span data-ttu-id="aafd4-111">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="aafd4-111">Output : 'T[]</span></span>

<span data-ttu-id="aafd4-112">Uma matriz `'T[]` de elementos que satisfazem o predicado.</span><span class="sxs-lookup"><span data-stu-id="aafd4-112">An array `'T[]` of elements that satisfy the predicate.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="aafd4-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="aafd4-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="aafd4-114">T'</span><span class="sxs-lookup"><span data-stu-id="aafd4-114">'T</span></span>

<span data-ttu-id="aafd4-115">O tipo de `array` elementos.</span><span class="sxs-lookup"><span data-stu-id="aafd4-115">The type of `array` elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="aafd4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="aafd4-116">Remarks</span></span>

<span data-ttu-id="aafd4-117">A função é definida para tipos genéricos, ou seja, sempre que temos uma matriz `'T[]` e um predicado, `'T -> Bool` podemos filtrar elementos.</span><span class="sxs-lookup"><span data-stu-id="aafd4-117">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a predicate `'T -> Bool` we can filter elements.</span></span>