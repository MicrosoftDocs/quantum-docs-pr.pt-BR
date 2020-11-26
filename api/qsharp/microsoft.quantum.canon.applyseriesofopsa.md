---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsA
title: Operação ApplySeriesOfOpsA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsA
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Adjoint)
ms.openlocfilehash: e5b3527507f79dcc77803ce01472856145df0e9f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217961"
---
# <a name="applyseriesofopsa-operation"></a><span data-ttu-id="601d9-102">Operação ApplySeriesOfOpsA</span><span class="sxs-lookup"><span data-stu-id="601d9-102">ApplySeriesOfOpsA operation</span></span>

<span data-ttu-id="601d9-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="601d9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="601d9-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="601d9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="601d9-105">Aplica uma lista de operações e seus destinos seqüencialmente em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="601d9-105">Applies a list of ops and their targets sequentially on an array.</span></span> <span data-ttu-id="601d9-106">(Adjacente)</span><span class="sxs-lookup"><span data-stu-id="601d9-106">(Adjoint)</span></span>

```qsharp
operation ApplySeriesOfOpsA<'T> (listOfOps : ('T[] => Unit is Adj)[], targets : Int[][], register : 'T[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="601d9-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="601d9-107">Input</span></span>

### <a name="listofops--t--unit--is-adj"></a><span data-ttu-id="601d9-108">listOfOps: t [] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj []</span><span class="sxs-lookup"><span data-stu-id="601d9-108">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj[]</span></span>

<span data-ttu-id="601d9-109">Lista de operações, cada uma levando uma matriz não, a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="601d9-109">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="601d9-110">Eles são aplicados em sequência, o índice mais baixo primeiro.</span><span class="sxs-lookup"><span data-stu-id="601d9-110">They are applied sequentially, lowest index first.</span></span>
<span data-ttu-id="601d9-111">Cada um deve ter um functor adjacente</span><span class="sxs-lookup"><span data-stu-id="601d9-111">Each must have an adjoint functor</span></span>


### <a name="targets--int"></a><span data-ttu-id="601d9-112">destinos: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="601d9-112">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="601d9-113">Matrizes aninhadas que descrevem os destinos da operação.</span><span class="sxs-lookup"><span data-stu-id="601d9-113">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="601d9-114">Cada matriz deve conter uma lista de ints descrevendo os índices a serem usados.</span><span class="sxs-lookup"><span data-stu-id="601d9-114">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="601d9-115">registrar: t []</span><span class="sxs-lookup"><span data-stu-id="601d9-115">register : 'T[]</span></span>

<span data-ttu-id="601d9-116">Qubit registrar-se para ser tratado.</span><span class="sxs-lookup"><span data-stu-id="601d9-116">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="601d9-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="601d9-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="601d9-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="601d9-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="601d9-119">T'</span><span class="sxs-lookup"><span data-stu-id="601d9-119">'T</span></span>



## <a name="see-also"></a><span data-ttu-id="601d9-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="601d9-120">See Also</span></span>

- [<span data-ttu-id="601d9-121">Microsoft. Quantum. Canon. ApplyOpRepeatedlyOver</span><span class="sxs-lookup"><span data-stu-id="601d9-121">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)