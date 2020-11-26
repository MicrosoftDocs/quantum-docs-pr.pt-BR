---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsC
title: Operação ApplySeriesOfOpsC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsC
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Controlled)
ms.openlocfilehash: eaa0ea3e33cce708af5879cfbe875397fbb82a8a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217927"
---
# <a name="applyseriesofopsc-operation"></a><span data-ttu-id="8f025-102">Operação ApplySeriesOfOpsC</span><span class="sxs-lookup"><span data-stu-id="8f025-102">ApplySeriesOfOpsC operation</span></span>

<span data-ttu-id="8f025-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8f025-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8f025-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8f025-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8f025-105">Aplica uma lista de operações e seus destinos seqüencialmente em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="8f025-105">Applies a list of ops and their targets sequentially on an array.</span></span> <span data-ttu-id="8f025-106">Controlado</span><span class="sxs-lookup"><span data-stu-id="8f025-106">(Controlled)</span></span>

```qsharp
operation ApplySeriesOfOpsC<'T> (listOfOps : ('T[] => Unit is Ctl)[], targets : Int[][], register : 'T[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="8f025-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="8f025-107">Input</span></span>

### <a name="listofops--t--unit--is-ctl"></a><span data-ttu-id="8f025-108">listOfOps: t [] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é CTL []</span><span class="sxs-lookup"><span data-stu-id="8f025-108">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl[]</span></span>

<span data-ttu-id="8f025-109">Lista de operações, cada uma levando uma matriz não, a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="8f025-109">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="8f025-110">Eles são aplicados em sequência, o índice mais baixo primeiro.</span><span class="sxs-lookup"><span data-stu-id="8f025-110">They are applied sequentially, lowest index first.</span></span>
<span data-ttu-id="8f025-111">Cada um deve ter um functor controlado</span><span class="sxs-lookup"><span data-stu-id="8f025-111">Each must have a Controlled functor</span></span>


### <a name="targets--int"></a><span data-ttu-id="8f025-112">destinos: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="8f025-112">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="8f025-113">Matrizes aninhadas que descrevem os destinos da operação.</span><span class="sxs-lookup"><span data-stu-id="8f025-113">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="8f025-114">Cada matriz deve conter uma lista de ints descrevendo os índices a serem usados.</span><span class="sxs-lookup"><span data-stu-id="8f025-114">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="8f025-115">registrar: t []</span><span class="sxs-lookup"><span data-stu-id="8f025-115">register : 'T[]</span></span>

<span data-ttu-id="8f025-116">Qubit registrar-se para ser tratado.</span><span class="sxs-lookup"><span data-stu-id="8f025-116">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8f025-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8f025-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="8f025-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="8f025-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8f025-119">T'</span><span class="sxs-lookup"><span data-stu-id="8f025-119">'T</span></span>



## <a name="see-also"></a><span data-ttu-id="8f025-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="8f025-120">See Also</span></span>

- [<span data-ttu-id="8f025-121">Microsoft. Quantum. Canon. ApplyOpRepeatedlyOver</span><span class="sxs-lookup"><span data-stu-id="8f025-121">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)