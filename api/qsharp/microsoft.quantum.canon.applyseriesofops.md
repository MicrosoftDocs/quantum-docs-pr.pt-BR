---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOps
title: Operação ApplySeriesOfOps
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOps
qsharp.summary: Applies a list of ops and their targets sequentially on an array.
ms.openlocfilehash: b8810e7d31689046e72905195a3a25ef80fc8d67
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217995"
---
# <a name="applyseriesofops-operation"></a><span data-ttu-id="0c1db-102">Operação ApplySeriesOfOps</span><span class="sxs-lookup"><span data-stu-id="0c1db-102">ApplySeriesOfOps operation</span></span>

<span data-ttu-id="0c1db-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0c1db-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0c1db-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0c1db-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0c1db-105">Aplica uma lista de operações e seus destinos seqüencialmente em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="0c1db-105">Applies a list of ops and their targets sequentially on an array.</span></span>

```qsharp
operation ApplySeriesOfOps<'T> (listOfOps : ('T[] => Unit)[], targets : Int[][], register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="0c1db-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="0c1db-106">Input</span></span>

### <a name="listofops--t--unit-"></a><span data-ttu-id="0c1db-107">listOfOps: t [] => [unidade](xref:microsoft.quantum.lang-ref.unit) []</span><span class="sxs-lookup"><span data-stu-id="0c1db-107">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span></span>

<span data-ttu-id="0c1db-108">Lista de operações, cada uma levando uma matriz não, a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="0c1db-108">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="0c1db-109">Eles são aplicados em sequência, o índice mais baixo primeiro.</span><span class="sxs-lookup"><span data-stu-id="0c1db-109">They are applied sequentially, lowest index first.</span></span>


### <a name="targets--int"></a><span data-ttu-id="0c1db-110">destinos: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="0c1db-110">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="0c1db-111">Matrizes aninhadas que descrevem os destinos da operação.</span><span class="sxs-lookup"><span data-stu-id="0c1db-111">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="0c1db-112">Cada matriz deve conter uma lista de ints descrevendo os índices a serem usados.</span><span class="sxs-lookup"><span data-stu-id="0c1db-112">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="0c1db-113">registrar: t []</span><span class="sxs-lookup"><span data-stu-id="0c1db-113">register : 'T[]</span></span>

<span data-ttu-id="0c1db-114">Qubit registrar-se para ser tratado.</span><span class="sxs-lookup"><span data-stu-id="0c1db-114">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0c1db-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0c1db-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="0c1db-116">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="0c1db-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0c1db-117">T'</span><span class="sxs-lookup"><span data-stu-id="0c1db-117">'T</span></span>



## <a name="see-also"></a><span data-ttu-id="0c1db-118">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="0c1db-118">See Also</span></span>

- [<span data-ttu-id="0c1db-119">Microsoft. Quantum. Canon. ApplyOpRepeatedlyOver</span><span class="sxs-lookup"><span data-stu-id="0c1db-119">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)