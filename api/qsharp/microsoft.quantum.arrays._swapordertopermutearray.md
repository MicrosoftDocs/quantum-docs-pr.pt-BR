---
uid: Microsoft.Quantum.Arrays._SwapOrderToPermuteArray
title: Função _SwapOrderToPermuteArray
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: _SwapOrderToPermuteArray
qsharp.summary: Returns the order elements in an array need to be swapped to produce an ordered array. Assumes swaps occur in place.
ms.openlocfilehash: 965f2f3d4f8b366abb27287ce0d27a3b7d7b8fb8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694513"
---
# <a name="_swapordertopermutearray-function"></a><span data-ttu-id="200cf-102">Função _SwapOrderToPermuteArray</span><span class="sxs-lookup"><span data-stu-id="200cf-102">_SwapOrderToPermuteArray function</span></span>

<span data-ttu-id="200cf-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="200cf-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="200cf-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="200cf-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="200cf-105">Retorna os elementos de ordem em uma matriz que precisam ser trocados para produzir uma matriz ordenada.</span><span class="sxs-lookup"><span data-stu-id="200cf-105">Returns the order elements in an array need to be swapped to produce an ordered array.</span></span>
<span data-ttu-id="200cf-106">Pressupõe que as trocas ocorrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="200cf-106">Assumes swaps occur in place.</span></span>

```qsharp
function _SwapOrderToPermuteArray (newOrder : Int[]) : (Int, Int)[]
```


## <a name="input"></a><span data-ttu-id="200cf-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="200cf-107">Input</span></span>

### <a name="neworder--int"></a><span data-ttu-id="200cf-108">newOrder: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="200cf-108">newOrder : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="200cf-109">Matriz com a permutação dos índices da nova matriz.</span><span class="sxs-lookup"><span data-stu-id="200cf-109">Array with the permutation of the indices of the new array.</span></span> <span data-ttu-id="200cf-110">Deve haver $n elementos $, cada um com um inteiro exclusivo de $0 $ a $n-$1.</span><span class="sxs-lookup"><span data-stu-id="200cf-110">There should be $n$ elements, each being a unique integer from $0$ to $n-1$.</span></span>



## <a name="output--intint"></a><span data-ttu-id="200cf-111">Saída: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="200cf-111">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>

<span data-ttu-id="200cf-112">A tupla representa os dois índices a serem trocados.</span><span class="sxs-lookup"><span data-stu-id="200cf-112">The tuple represents the two indices to be swapped.</span></span> <span data-ttu-id="200cf-113">As trocas começam no índice mais baixo.</span><span class="sxs-lookup"><span data-stu-id="200cf-113">The swaps begin at the lowest index.</span></span>

## <a name="remarks"></a><span data-ttu-id="200cf-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="200cf-114">Remarks</span></span>

## <a name="psuedocode"></a><span data-ttu-id="200cf-115">Psuedocode</span><span class="sxs-lookup"><span data-stu-id="200cf-115">Psuedocode</span></span>

<span data-ttu-id="200cf-116">para (índice em 0.. Length (newOrder)-1) {enquanto newOrder [index]! = index {switch newOrder [index] with newOrder [newOrder [index]]}}</span><span class="sxs-lookup"><span data-stu-id="200cf-116">for (index in 0..Length(newOrder) - 1) { while newOrder[index] != index { Switch newOrder[index] with newOrder[newOrder[index]] } }</span></span>