---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsCA
title: Operação ApplySeriesOfOpsCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsCA
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Adjoint + Controlled)
ms.openlocfilehash: 9a1f6189428b086c38b1d0f289afb18c2cf1be40
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850864"
---
# <a name="applyseriesofopsca-operation"></a><span data-ttu-id="12d82-102">Operação ApplySeriesOfOpsCA</span><span class="sxs-lookup"><span data-stu-id="12d82-102">ApplySeriesOfOpsCA operation</span></span>

<span data-ttu-id="12d82-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="12d82-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="12d82-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="12d82-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="12d82-105">Aplica uma lista de operações e seus destinos seqüencialmente em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="12d82-105">Applies a list of ops and their targets sequentially on an array.</span></span> <span data-ttu-id="12d82-106">(Adjacente + controlado)</span><span class="sxs-lookup"><span data-stu-id="12d82-106">(Adjoint + Controlled)</span></span>

```qsharp
operation ApplySeriesOfOpsCA<'T> (listOfOps : ('T[] => Unit is Adj + Ctl)[], targets : Int[][], register : 'T[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="12d82-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="12d82-107">Input</span></span>

### <a name="listofops--t--unit--is-adj--ctl"></a><span data-ttu-id="12d82-108">listOfOps: t [] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL []</span><span class="sxs-lookup"><span data-stu-id="12d82-108">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl[]</span></span>

<span data-ttu-id="12d82-109">Lista de operações, cada uma levando uma matriz não, a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="12d82-109">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="12d82-110">Eles são aplicados em sequência, o índice mais baixo primeiro.</span><span class="sxs-lookup"><span data-stu-id="12d82-110">They are applied sequentially, lowest index first.</span></span>
<span data-ttu-id="12d82-111">Cada um deve ter um functor controlado e um de controle.</span><span class="sxs-lookup"><span data-stu-id="12d82-111">Each must have both an Adjoint and Controlled functor.</span></span>


### <a name="targets--int"></a><span data-ttu-id="12d82-112">destinos: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="12d82-112">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="12d82-113">Matrizes aninhadas que descrevem os destinos da operação.</span><span class="sxs-lookup"><span data-stu-id="12d82-113">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="12d82-114">Cada matriz deve conter uma lista de ints descrevendo os índices a serem usados.</span><span class="sxs-lookup"><span data-stu-id="12d82-114">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="12d82-115">registrar: t []</span><span class="sxs-lookup"><span data-stu-id="12d82-115">register : 'T[]</span></span>

<span data-ttu-id="12d82-116">Qubit registrar-se para ser tratado.</span><span class="sxs-lookup"><span data-stu-id="12d82-116">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="12d82-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="12d82-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="12d82-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="12d82-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="12d82-119">T'</span><span class="sxs-lookup"><span data-stu-id="12d82-119">'T</span></span>



## <a name="example"></a><span data-ttu-id="12d82-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="12d82-120">Example</span></span>

<span data-ttu-id="12d82-121">O seguinte aplica-se exp ([PauliX, PauliY], 0,5) a qubits 0, 1//then X para qubit 2 Let Ops = [exp ([PauliX, PauliY], 0,5, _), ApplyToFirstQubitCA (X, _)]; permitir índices = [[0, 1], [2]]; ApplySeriesOfOpsCA (Ops, índices, qubitArray);</span><span class="sxs-lookup"><span data-stu-id="12d82-121">// The following applies Exp([PauliX, PauliY], 0.5) to qubits 0, 1 // then X to qubit 2 let ops = [Exp([PauliX, PauliY], 0.5, _), ApplyToFirstQubitCA(X, _)]; let indices = [[0, 1], [2]]; ApplySeriesOfOpsCA(ops, indices, qubitArray);</span></span>

## <a name="see-also"></a><span data-ttu-id="12d82-122">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="12d82-122">See Also</span></span>

- [<span data-ttu-id="12d82-123">Microsoft. Quantum. Canon. ApplyOpRepeatedlyOver</span><span class="sxs-lookup"><span data-stu-id="12d82-123">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)