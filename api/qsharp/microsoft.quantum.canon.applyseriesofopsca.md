---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsCA
title: Operação ApplySeriesOfOpsCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsCA
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Adjoint + Controlled)
ms.openlocfilehash: 2327a693e528cf46f95eae5ee052e9dd9b6ee187
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694217"
---
# <a name="applyseriesofopsca-operation"></a><span data-ttu-id="aea94-102">Operação ApplySeriesOfOpsCA</span><span class="sxs-lookup"><span data-stu-id="aea94-102">ApplySeriesOfOpsCA operation</span></span>

<span data-ttu-id="aea94-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="aea94-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="aea94-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="aea94-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="aea94-105">Aplica uma lista de operações e seus destinos seqüencialmente em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="aea94-105">Applies a list of ops and their targets sequentially on an array.</span></span> <span data-ttu-id="aea94-106">(Adjacente + controlado)</span><span class="sxs-lookup"><span data-stu-id="aea94-106">(Adjoint + Controlled)</span></span>

```qsharp
operation ApplySeriesOfOpsCA<'T> (listOfOps : ('T[] => Unit is Adj + Ctl)[], targets : Int[][], register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="aea94-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="aea94-107">Input</span></span>

### <a name="listofops--t--unit-adj--ctl"></a><span data-ttu-id="aea94-108">listOfOps: t [] => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL []</span><span class="sxs-lookup"><span data-stu-id="aea94-108">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl[]</span></span>

<span data-ttu-id="aea94-109">Lista de operações, cada uma levando uma matriz não, a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="aea94-109">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="aea94-110">Eles são aplicados em sequência, o índice mais baixo primeiro.</span><span class="sxs-lookup"><span data-stu-id="aea94-110">They are applied sequentially, lowest index first.</span></span>
<span data-ttu-id="aea94-111">Cada um deve ter um functor controlado e um de controle.</span><span class="sxs-lookup"><span data-stu-id="aea94-111">Each must have both an Adjoint and Controlled functor.</span></span>


### <a name="targets--int"></a><span data-ttu-id="aea94-112">destinos: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="aea94-112">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="aea94-113">Matrizes aninhadas que descrevem os destinos da operação.</span><span class="sxs-lookup"><span data-stu-id="aea94-113">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="aea94-114">Cada matriz deve conter uma lista de ints descrevendo os índices a serem usados.</span><span class="sxs-lookup"><span data-stu-id="aea94-114">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="aea94-115">registrar: t []</span><span class="sxs-lookup"><span data-stu-id="aea94-115">register : 'T[]</span></span>

<span data-ttu-id="aea94-116">Qubit registrar-se para ser tratado.</span><span class="sxs-lookup"><span data-stu-id="aea94-116">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="aea94-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="aea94-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="aea94-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="aea94-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="aea94-119">T'</span><span class="sxs-lookup"><span data-stu-id="aea94-119">'T</span></span>



## <a name="see-also"></a><span data-ttu-id="aea94-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="aea94-120">See Also</span></span>

- [<span data-ttu-id="aea94-121">Microsoft. Quantum. Canon. ApplyOpRepeatedlyOver</span><span class="sxs-lookup"><span data-stu-id="aea94-121">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)