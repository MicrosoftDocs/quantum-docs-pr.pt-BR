---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianProduct
title: Operação IterateThroughCartesianProduct
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianProduct
qsharp.summary: Applies an operation for each index in the Cartesian product of several ranges.
ms.openlocfilehash: 6340c7a972253e6f583a3856df93a7066ced3139
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206435"
---
# <a name="iteratethroughcartesianproduct-operation"></a><span data-ttu-id="f54e3-102">Operação IterateThroughCartesianProduct</span><span class="sxs-lookup"><span data-stu-id="f54e3-102">IterateThroughCartesianProduct operation</span></span>

<span data-ttu-id="f54e3-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f54e3-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f54e3-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f54e3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f54e3-105">Aplica uma operação para cada índice no produto cartesiano de vários intervalos.</span><span class="sxs-lookup"><span data-stu-id="f54e3-105">Applies an operation for each index in the Cartesian product of several ranges.</span></span>

```qsharp
operation IterateThroughCartesianProduct (bounds : Int[], op : (Int[] => Unit)) : Unit
```


## <a name="description"></a><span data-ttu-id="f54e3-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="f54e3-106">Description</span></span>

<span data-ttu-id="f54e3-107">Aplica iterativamente uma operação para cada elemento do produto cartesiano de `0..(bounds[0] - 1)` , `0..(bounds[1] - 1)` ,..., `0..(bounds[Length(bounds) - 1] - 1)`</span><span class="sxs-lookup"><span data-stu-id="f54e3-107">Iteratively applies an operation for each element of the Cartesian product of `0..(bounds[0] - 1)`, `0..(bounds[1] - 1)`, ..., `0..(bounds[Length(bounds) - 1] - 1)`</span></span>

## <a name="input"></a><span data-ttu-id="f54e3-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="f54e3-108">Input</span></span>

### <a name="bounds--int"></a><span data-ttu-id="f54e3-109">limites: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="f54e3-109">bounds : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="f54e3-110">Uma matriz que especifica os intervalos a serem iterados, com cada intervalo sendo especificado como um comprimento inteiro.</span><span class="sxs-lookup"><span data-stu-id="f54e3-110">An array specifying the ranges to be iterated over, with each range being specified as an integer length.</span></span>


### <a name="op--int--unit"></a><span data-ttu-id="f54e3-111">op: [int](xref:microsoft.quantum.lang-ref.int)[] = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="f54e3-111">op : [Int](xref:microsoft.quantum.lang-ref.int)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="f54e3-112">Uma operação a ser chamada para cada elemento do produto cartesiano fornecido.</span><span class="sxs-lookup"><span data-stu-id="f54e3-112">An operation to be called for each element of the given Cartesian product.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f54e3-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f54e3-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="f54e3-114">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="f54e3-114">See Also</span></span>

- [<span data-ttu-id="f54e3-115">Microsoft. Quantum. Canon. IterateThroughCartesianPower</span><span class="sxs-lookup"><span data-stu-id="f54e3-115">Microsoft.Quantum.Canon.IterateThroughCartesianPower</span></span>](xref:Microsoft.Quantum.Canon.IterateThroughCartesianPower)