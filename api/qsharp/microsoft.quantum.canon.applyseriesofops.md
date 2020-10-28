---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOps
title: Operação ApplySeriesOfOps
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOps
qsharp.summary: Applies a list of ops and their targets sequentially on an array.
ms.openlocfilehash: aff0bcb831960153166e88aef1f05e000125d5d8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694222"
---
# <a name="applyseriesofops-operation"></a><span data-ttu-id="3df63-102">Operação ApplySeriesOfOps</span><span class="sxs-lookup"><span data-stu-id="3df63-102">ApplySeriesOfOps operation</span></span>

<span data-ttu-id="3df63-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="3df63-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="3df63-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3df63-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3df63-105">Aplica uma lista de operações e seus destinos seqüencialmente em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="3df63-105">Applies a list of ops and their targets sequentially on an array.</span></span>

```qsharp
operation ApplySeriesOfOps<'T> (listOfOps : ('T[] => Unit)[], targets : Int[][], register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="3df63-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="3df63-106">Input</span></span>

### <a name="listofops--t--unit-"></a><span data-ttu-id="3df63-107">listOfOps: t [] => [unidade](xref:microsoft.quantum.lang-ref.unit) []</span><span class="sxs-lookup"><span data-stu-id="3df63-107">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span></span>

<span data-ttu-id="3df63-108">Lista de operações, cada uma levando uma matriz não, a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="3df63-108">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="3df63-109">Eles são aplicados em sequência, o índice mais baixo primeiro.</span><span class="sxs-lookup"><span data-stu-id="3df63-109">They are applied sequentially, lowest index first.</span></span>


### <a name="targets--int"></a><span data-ttu-id="3df63-110">destinos: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="3df63-110">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="3df63-111">Matrizes aninhadas que descrevem os destinos da operação.</span><span class="sxs-lookup"><span data-stu-id="3df63-111">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="3df63-112">Cada matriz deve conter uma lista de ints descrevendo os índices a serem usados.</span><span class="sxs-lookup"><span data-stu-id="3df63-112">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="3df63-113">registrar: t []</span><span class="sxs-lookup"><span data-stu-id="3df63-113">register : 'T[]</span></span>

<span data-ttu-id="3df63-114">Qubit registrar-se para ser tratado.</span><span class="sxs-lookup"><span data-stu-id="3df63-114">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3df63-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3df63-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="3df63-116">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="3df63-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3df63-117">T'</span><span class="sxs-lookup"><span data-stu-id="3df63-117">'T</span></span>



## <a name="see-also"></a><span data-ttu-id="3df63-118">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="3df63-118">See Also</span></span>

- [<span data-ttu-id="3df63-119">Microsoft. Quantum. Canon. ApplyOpRepeatedlyOver</span><span class="sxs-lookup"><span data-stu-id="3df63-119">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)