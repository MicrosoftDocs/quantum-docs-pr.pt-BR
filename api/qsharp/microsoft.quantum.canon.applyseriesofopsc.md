---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsC
title: Operação ApplySeriesOfOpsC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsC
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Controlled)
ms.openlocfilehash: d909aadbfe86f6d1314e9be5434249c40932ae4a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694219"
---
# <a name="applyseriesofopsc-operation"></a><span data-ttu-id="736a4-102">Operação ApplySeriesOfOpsC</span><span class="sxs-lookup"><span data-stu-id="736a4-102">ApplySeriesOfOpsC operation</span></span>

<span data-ttu-id="736a4-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="736a4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="736a4-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="736a4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="736a4-105">Aplica uma lista de operações e seus destinos seqüencialmente em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="736a4-105">Applies a list of ops and their targets sequentially on an array.</span></span> <span data-ttu-id="736a4-106">Controlado</span><span class="sxs-lookup"><span data-stu-id="736a4-106">(Controlled)</span></span>

```qsharp
operation ApplySeriesOfOpsC<'T> (listOfOps : ('T[] => Unit is Ctl)[], targets : Int[][], register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="736a4-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="736a4-107">Input</span></span>

### <a name="listofops--t--unit-ctl"></a><span data-ttu-id="736a4-108">listOfOps: t [] => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit) []</span><span class="sxs-lookup"><span data-stu-id="736a4-108">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl[]</span></span>

<span data-ttu-id="736a4-109">Lista de operações, cada uma levando uma matriz não, a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="736a4-109">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="736a4-110">Eles são aplicados em sequência, o índice mais baixo primeiro.</span><span class="sxs-lookup"><span data-stu-id="736a4-110">They are applied sequentially, lowest index first.</span></span>
<span data-ttu-id="736a4-111">Cada um deve ter um functor controlado</span><span class="sxs-lookup"><span data-stu-id="736a4-111">Each must have a Controlled functor</span></span>


### <a name="targets--int"></a><span data-ttu-id="736a4-112">destinos: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="736a4-112">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="736a4-113">Matrizes aninhadas que descrevem os destinos da operação.</span><span class="sxs-lookup"><span data-stu-id="736a4-113">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="736a4-114">Cada matriz deve conter uma lista de ints descrevendo os índices a serem usados.</span><span class="sxs-lookup"><span data-stu-id="736a4-114">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="736a4-115">registrar: t []</span><span class="sxs-lookup"><span data-stu-id="736a4-115">register : 'T[]</span></span>

<span data-ttu-id="736a4-116">Qubit registrar-se para ser tratado.</span><span class="sxs-lookup"><span data-stu-id="736a4-116">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="736a4-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="736a4-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="736a4-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="736a4-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="736a4-119">T'</span><span class="sxs-lookup"><span data-stu-id="736a4-119">'T</span></span>



## <a name="see-also"></a><span data-ttu-id="736a4-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="736a4-120">See Also</span></span>

- [<span data-ttu-id="736a4-121">Microsoft. Quantum. Canon. ApplyOpRepeatedlyOver</span><span class="sxs-lookup"><span data-stu-id="736a4-121">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)