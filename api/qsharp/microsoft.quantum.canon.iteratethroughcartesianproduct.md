---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianProduct
title: Operação IterateThroughCartesianProduct
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianProduct
qsharp.summary: Applies an operation for each index in the Cartesian product of several ranges.
ms.openlocfilehash: a0aaa8ef6aa6798d31c810254c92820f8136800c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840274"
---
# <a name="iteratethroughcartesianproduct-operation"></a><span data-ttu-id="aaffe-102">Operação IterateThroughCartesianProduct</span><span class="sxs-lookup"><span data-stu-id="aaffe-102">IterateThroughCartesianProduct operation</span></span>

<span data-ttu-id="aaffe-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="aaffe-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="aaffe-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="aaffe-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="aaffe-105">Aplica uma operação para cada índice no produto cartesiano de vários intervalos.</span><span class="sxs-lookup"><span data-stu-id="aaffe-105">Applies an operation for each index in the Cartesian product of several ranges.</span></span>

```qsharp
operation IterateThroughCartesianProduct (bounds : Int[], op : (Int[] => Unit)) : Unit
```


## <a name="description"></a><span data-ttu-id="aaffe-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="aaffe-106">Description</span></span>

<span data-ttu-id="aaffe-107">Aplica iterativamente uma operação para cada elemento do produto cartesiano de `0..(bounds[0] - 1)` , `0..(bounds[1] - 1)` ,..., `0..(bounds[Length(bounds) - 1] - 1)`</span><span class="sxs-lookup"><span data-stu-id="aaffe-107">Iteratively applies an operation for each element of the Cartesian product of `0..(bounds[0] - 1)`, `0..(bounds[1] - 1)`, ..., `0..(bounds[Length(bounds) - 1] - 1)`</span></span>

## <a name="input"></a><span data-ttu-id="aaffe-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="aaffe-108">Input</span></span>

### <a name="bounds--int"></a><span data-ttu-id="aaffe-109">limites: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="aaffe-109">bounds : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="aaffe-110">Uma matriz que especifica os intervalos a serem iterados, com cada intervalo sendo especificado como um comprimento inteiro.</span><span class="sxs-lookup"><span data-stu-id="aaffe-110">An array specifying the ranges to be iterated over, with each range being specified as an integer length.</span></span>


### <a name="op--int--unit"></a><span data-ttu-id="aaffe-111">op: [int](xref:microsoft.quantum.lang-ref.int)[] = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="aaffe-111">op : [Int](xref:microsoft.quantum.lang-ref.int)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="aaffe-112">Uma operação a ser chamada para cada elemento do produto cartesiano fornecido.</span><span class="sxs-lookup"><span data-stu-id="aaffe-112">An operation to be called for each element of the given Cartesian product.</span></span>



## <a name="output--unit"></a><span data-ttu-id="aaffe-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="aaffe-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="aaffe-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="aaffe-114">Example</span></span>

<span data-ttu-id="aaffe-115">Dada uma operação `op` , os dois trechos de código a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="aaffe-115">Given an operation `op`, the following two snippets are equivalent:</span></span>

```qsharp
IterateThroughCartesianProduct([3, 4, 5], op);
```

```qsharp
op([0, 0, 0]);
op([1, 0, 0]);
op([2, 0, 0]);
op([0, 1, 0]);
// ...
op([0, 3, 0]);
op([0, 0, 1]);
//
op([2, 3, 4]);
```

## <a name="see-also"></a><span data-ttu-id="aaffe-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="aaffe-116">See Also</span></span>

- [<span data-ttu-id="aaffe-117">Microsoft. Quantum. Canon. IterateThroughCartesianPower</span><span class="sxs-lookup"><span data-stu-id="aaffe-117">Microsoft.Quantum.Canon.IterateThroughCartesianPower</span></span>](xref:Microsoft.Quantum.Canon.IterateThroughCartesianPower)