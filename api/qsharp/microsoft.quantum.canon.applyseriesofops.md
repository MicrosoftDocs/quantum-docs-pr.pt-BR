---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOps
title: Operação ApplySeriesOfOps
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOps
qsharp.summary: Applies a list of ops and their targets sequentially on an array.
ms.openlocfilehash: b086b01b0be86bd25a6d6cdef26bfbb53e484cb2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841509"
---
# <a name="applyseriesofops-operation"></a><span data-ttu-id="f47d4-102">Operação ApplySeriesOfOps</span><span class="sxs-lookup"><span data-stu-id="f47d4-102">ApplySeriesOfOps operation</span></span>

<span data-ttu-id="f47d4-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f47d4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f47d4-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f47d4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f47d4-105">Aplica uma lista de operações e seus destinos seqüencialmente em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="f47d4-105">Applies a list of ops and their targets sequentially on an array.</span></span>

```qsharp
operation ApplySeriesOfOps<'T> (listOfOps : ('T[] => Unit)[], targets : Int[][], register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="f47d4-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="f47d4-106">Input</span></span>

### <a name="listofops--t--unit-"></a><span data-ttu-id="f47d4-107">listOfOps: t [] => [unidade](xref:microsoft.quantum.lang-ref.unit) []</span><span class="sxs-lookup"><span data-stu-id="f47d4-107">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span></span>

<span data-ttu-id="f47d4-108">Lista de operações, cada uma levando uma matriz não, a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="f47d4-108">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="f47d4-109">Eles são aplicados em sequência, o índice mais baixo primeiro.</span><span class="sxs-lookup"><span data-stu-id="f47d4-109">They are applied sequentially, lowest index first.</span></span>


### <a name="targets--int"></a><span data-ttu-id="f47d4-110">destinos: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="f47d4-110">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="f47d4-111">Matrizes aninhadas que descrevem os destinos da operação.</span><span class="sxs-lookup"><span data-stu-id="f47d4-111">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="f47d4-112">Cada matriz deve conter uma lista de ints descrevendo os índices a serem usados.</span><span class="sxs-lookup"><span data-stu-id="f47d4-112">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="f47d4-113">registrar: t []</span><span class="sxs-lookup"><span data-stu-id="f47d4-113">register : 'T[]</span></span>

<span data-ttu-id="f47d4-114">Qubit registrar-se para ser tratado.</span><span class="sxs-lookup"><span data-stu-id="f47d4-114">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f47d4-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f47d4-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f47d4-116">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="f47d4-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f47d4-117">T'</span><span class="sxs-lookup"><span data-stu-id="f47d4-117">'T</span></span>



## <a name="example"></a><span data-ttu-id="f47d4-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="f47d4-118">Example</span></span>

<span data-ttu-id="f47d4-119">O seguinte aplica-se exp ([PauliX, PauliY], 0,5) a qubits 0, 1//then X para qubit 2 Let Ops = [exp ([PauliX, PauliY], 0,5, _), ApplyToFirstQubit (X, _)]; permitir índices = [[0, 1], [2]]; ApplySeriesOfOps (Ops, índices, qubitArray);</span><span class="sxs-lookup"><span data-stu-id="f47d4-119">// The following applies Exp([PauliX, PauliY], 0.5) to qubits 0, 1 // then X to qubit 2 let ops = [Exp([PauliX, PauliY], 0.5, _), ApplyToFirstQubit(X, _)]; let indices = [[0, 1], [2]]; ApplySeriesOfOps(ops, indices, qubitArray);</span></span>

## <a name="see-also"></a><span data-ttu-id="f47d4-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="f47d4-120">See Also</span></span>

- [<span data-ttu-id="f47d4-121">Microsoft. Quantum. Canon. ApplyOpRepeatedlyOver</span><span class="sxs-lookup"><span data-stu-id="f47d4-121">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)