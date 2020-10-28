---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsA
title: Operação ApplySeriesOfOpsA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsA
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Adjoint)
ms.openlocfilehash: e2b928fa4c9446e16d2bf5e7b68a32d4bba3a528
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694220"
---
# <a name="applyseriesofopsa-operation"></a><span data-ttu-id="a736e-102">Operação ApplySeriesOfOpsA</span><span class="sxs-lookup"><span data-stu-id="a736e-102">ApplySeriesOfOpsA operation</span></span>

<span data-ttu-id="a736e-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a736e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a736e-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a736e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a736e-105">Aplica uma lista de operações e seus destinos seqüencialmente em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="a736e-105">Applies a list of ops and their targets sequentially on an array.</span></span> <span data-ttu-id="a736e-106">(Adjacente)</span><span class="sxs-lookup"><span data-stu-id="a736e-106">(Adjoint)</span></span>

```qsharp
operation ApplySeriesOfOpsA<'T> (listOfOps : ('T[] => Unit is Adj)[], targets : Int[][], register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="a736e-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="a736e-107">Input</span></span>

### <a name="listofops--t--unit-adj"></a><span data-ttu-id="a736e-108">listOfOps: t [] => ano da [unidade](xref:microsoft.quantum.lang-ref.unit) []</span><span class="sxs-lookup"><span data-stu-id="a736e-108">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj[]</span></span>

<span data-ttu-id="a736e-109">Lista de operações, cada uma levando uma matriz não, a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="a736e-109">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="a736e-110">Eles são aplicados em sequência, o índice mais baixo primeiro.</span><span class="sxs-lookup"><span data-stu-id="a736e-110">They are applied sequentially, lowest index first.</span></span>
<span data-ttu-id="a736e-111">Cada um deve ter um functor adjacente</span><span class="sxs-lookup"><span data-stu-id="a736e-111">Each must have an adjoint functor</span></span>


### <a name="targets--int"></a><span data-ttu-id="a736e-112">destinos: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="a736e-112">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="a736e-113">Matrizes aninhadas que descrevem os destinos da operação.</span><span class="sxs-lookup"><span data-stu-id="a736e-113">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="a736e-114">Cada matriz deve conter uma lista de ints descrevendo os índices a serem usados.</span><span class="sxs-lookup"><span data-stu-id="a736e-114">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="a736e-115">registrar: t []</span><span class="sxs-lookup"><span data-stu-id="a736e-115">register : 'T[]</span></span>

<span data-ttu-id="a736e-116">Qubit registrar-se para ser tratado.</span><span class="sxs-lookup"><span data-stu-id="a736e-116">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a736e-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a736e-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a736e-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="a736e-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a736e-119">T'</span><span class="sxs-lookup"><span data-stu-id="a736e-119">'T</span></span>



## <a name="see-also"></a><span data-ttu-id="a736e-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="a736e-120">See Also</span></span>

- [<span data-ttu-id="a736e-121">Microsoft. Quantum. Canon. ApplyOpRepeatedlyOver</span><span class="sxs-lookup"><span data-stu-id="a736e-121">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)