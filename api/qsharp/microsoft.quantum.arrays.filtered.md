---
uid: Microsoft.Quantum.Arrays.Filtered
title: Função filtrada
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Filtered
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, returns an array that consists of those elements that satisfy the predicate.
ms.openlocfilehash: 83336b7001ce1d8ab1f5340b194abdcf93588c31
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847156"
---
# <a name="filtered-function"></a><span data-ttu-id="d4985-102">Função filtrada</span><span class="sxs-lookup"><span data-stu-id="d4985-102">Filtered function</span></span>

<span data-ttu-id="d4985-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="d4985-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="d4985-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d4985-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d4985-105">Dada uma matriz e um predicado que é definido para os elementos da matriz, retorna uma matriz que consiste nesses elementos que atendem ao predicado.</span><span class="sxs-lookup"><span data-stu-id="d4985-105">Given an array and a predicate that is defined for the elements of the array, returns an array that consists of those elements that satisfy the predicate.</span></span>

```qsharp
function Filtered<'T> (predicate : ('T -> Bool), array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="d4985-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="d4985-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="d4985-107">predicado: [booliano](xref:microsoft.quantum.lang-ref.bool) -> bool</span><span class="sxs-lookup"><span data-stu-id="d4985-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="d4985-108">Uma função de `'T` para booliano que é usada para filtrar elementos.</span><span class="sxs-lookup"><span data-stu-id="d4985-108">A function from `'T` to Boolean that is used to filter elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="d4985-109">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="d4985-109">array : 'T[]</span></span>

<span data-ttu-id="d4985-110">Uma matriz de elementos `'T` .</span><span class="sxs-lookup"><span data-stu-id="d4985-110">An array of elements over `'T`.</span></span>



## <a name="output--t"></a><span data-ttu-id="d4985-111">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="d4985-111">Output : 'T[]</span></span>

<span data-ttu-id="d4985-112">Uma matriz `'T[]` de elementos que satisfazem o predicado.</span><span class="sxs-lookup"><span data-stu-id="d4985-112">An array `'T[]` of elements that satisfy the predicate.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d4985-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="d4985-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d4985-114">T'</span><span class="sxs-lookup"><span data-stu-id="d4985-114">'T</span></span>

<span data-ttu-id="d4985-115">O tipo de `array` elementos.</span><span class="sxs-lookup"><span data-stu-id="d4985-115">The type of `array` elements.</span></span>

## <a name="example"></a><span data-ttu-id="d4985-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d4985-116">Example</span></span>

<span data-ttu-id="d4985-117">O código a seguir demonstra a função "Filtered".</span><span class="sxs-lookup"><span data-stu-id="d4985-117">The following code demonstrates the "Filtered" function.</span></span>
<span data-ttu-id="d4985-118">Um predicado é definido usando a @"microsoft.quantum.logical.greaterthani" função:</span><span class="sxs-lookup"><span data-stu-id="d4985-118">A predicate is defined using the @"microsoft.quantum.logical.greaterthani" function:</span></span>

```qsharp
open Microsoft.Quantum.Arrays;
open Microsoft.Quantum.Logical;

function FilteredDemo() : Unit {
   let predicate = GreaterThanI(_, 5);
   let filteredArray = Filtered(predicate, [2, 5, 9, 1, 8]);
   Message($"{filteredArray}");
}
```

<span data-ttu-id="d4985-119">O resultado que um deve esperar deste exemplo será uma matriz de números maior que 5.</span><span class="sxs-lookup"><span data-stu-id="d4985-119">The outcome one should expect from this example will be an array of numbers greater than 5.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4985-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4985-120">Remarks</span></span>

<span data-ttu-id="d4985-121">A função é definida para tipos genéricos, ou seja, sempre que temos uma matriz `'T[]` e um predicado, `'T -> Bool` podemos filtrar elementos.</span><span class="sxs-lookup"><span data-stu-id="d4985-121">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a predicate `'T -> Bool` we can filter elements.</span></span>