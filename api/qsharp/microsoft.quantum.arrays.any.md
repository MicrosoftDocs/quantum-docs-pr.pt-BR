---
uid: Microsoft.Quantum.Arrays.Any
title: Qualquer função
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Any
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, checks if at least one element of the array satisfies the predicate.
ms.openlocfilehash: 717ab9ebcbb864a6faf1c14cd36125e589849f2e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221650"
---
# <a name="any-function"></a><span data-ttu-id="c6f01-102">Qualquer função</span><span class="sxs-lookup"><span data-stu-id="c6f01-102">Any function</span></span>

<span data-ttu-id="c6f01-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="c6f01-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="c6f01-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c6f01-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c6f01-105">Dada uma matriz e um predicado que é definido para os elementos da matriz, verifica se pelo menos um elemento da matriz atende ao predicado.</span><span class="sxs-lookup"><span data-stu-id="c6f01-105">Given an array and a predicate that is defined for the elements of the array, checks if at least one element of the array satisfies the predicate.</span></span>

```qsharp
function Any<'T> (predicate : ('T -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="c6f01-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="c6f01-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="c6f01-107">predicado: [booliano](xref:microsoft.quantum.lang-ref.bool) -> bool</span><span class="sxs-lookup"><span data-stu-id="c6f01-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="c6f01-108">Uma função de `'T` para `Bool` que é usada para verificar elementos.</span><span class="sxs-lookup"><span data-stu-id="c6f01-108">A function from `'T` to `Bool` that is used to check elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="c6f01-109">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="c6f01-109">array : 'T[]</span></span>

<span data-ttu-id="c6f01-110">Uma matriz de elementos `'T` .</span><span class="sxs-lookup"><span data-stu-id="c6f01-110">An array of elements over `'T`.</span></span>



## <a name="output--bool"></a><span data-ttu-id="c6f01-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="c6f01-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="c6f01-112">Um `Bool` valor da função or do predicado aplicado a todos os elementos.</span><span class="sxs-lookup"><span data-stu-id="c6f01-112">A `Bool` value of the OR function of the predicate applied to all elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="c6f01-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="c6f01-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c6f01-114">T'</span><span class="sxs-lookup"><span data-stu-id="c6f01-114">'T</span></span>

<span data-ttu-id="c6f01-115">O tipo de `array` elementos.</span><span class="sxs-lookup"><span data-stu-id="c6f01-115">The type of `array` elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6f01-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6f01-116">Remarks</span></span>

<span data-ttu-id="c6f01-117">A função é definida para tipos genéricos, ou seja, sempre que temos uma matriz `'T[]` e uma função, `predicate: 'T -> Bool` podemos produzir um `Bool` valor que indica se algum elemento atende `predicate` .</span><span class="sxs-lookup"><span data-stu-id="c6f01-117">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a function `predicate: 'T -> Bool` we can produce a `Bool` value that indicates if some element satisfies `predicate`.</span></span>