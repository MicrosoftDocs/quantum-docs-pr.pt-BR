---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsA
title: Operação ApplySeriesOfOpsA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsA
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Adjoint)
ms.openlocfilehash: 052cb52d4ee6500e60043ab7f808497058924afe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844660"
---
# <a name="applyseriesofopsa-operation"></a><span data-ttu-id="2c123-102">Operação ApplySeriesOfOpsA</span><span class="sxs-lookup"><span data-stu-id="2c123-102">ApplySeriesOfOpsA operation</span></span>

<span data-ttu-id="2c123-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="2c123-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="2c123-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2c123-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2c123-105">Aplica uma lista de operações e seus destinos seqüencialmente em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="2c123-105">Applies a list of ops and their targets sequentially on an array.</span></span> <span data-ttu-id="2c123-106">(Adjacente)</span><span class="sxs-lookup"><span data-stu-id="2c123-106">(Adjoint)</span></span>

```qsharp
operation ApplySeriesOfOpsA<'T> (listOfOps : ('T[] => Unit is Adj)[], targets : Int[][], register : 'T[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="2c123-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="2c123-107">Input</span></span>

### <a name="listofops--t--unit--is-adj"></a><span data-ttu-id="2c123-108">listOfOps: t [] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj []</span><span class="sxs-lookup"><span data-stu-id="2c123-108">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj[]</span></span>

<span data-ttu-id="2c123-109">Lista de operações, cada uma levando uma matriz não, a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="2c123-109">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="2c123-110">Eles são aplicados em sequência, o índice mais baixo primeiro.</span><span class="sxs-lookup"><span data-stu-id="2c123-110">They are applied sequentially, lowest index first.</span></span>
<span data-ttu-id="2c123-111">Cada um deve ter um functor adjacente</span><span class="sxs-lookup"><span data-stu-id="2c123-111">Each must have an adjoint functor</span></span>


### <a name="targets--int"></a><span data-ttu-id="2c123-112">destinos: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="2c123-112">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="2c123-113">Matrizes aninhadas que descrevem os destinos da operação.</span><span class="sxs-lookup"><span data-stu-id="2c123-113">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="2c123-114">Cada matriz deve conter uma lista de ints descrevendo os índices a serem usados.</span><span class="sxs-lookup"><span data-stu-id="2c123-114">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="2c123-115">registrar: t []</span><span class="sxs-lookup"><span data-stu-id="2c123-115">register : 'T[]</span></span>

<span data-ttu-id="2c123-116">Qubit registrar-se para ser tratado.</span><span class="sxs-lookup"><span data-stu-id="2c123-116">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2c123-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2c123-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="2c123-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="2c123-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2c123-119">T'</span><span class="sxs-lookup"><span data-stu-id="2c123-119">'T</span></span>



## <a name="example"></a><span data-ttu-id="2c123-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2c123-120">Example</span></span>

<span data-ttu-id="2c123-121">O seguinte aplica-se exp ([PauliX, PauliY], 0,5) a qubits 0, 1//then X para qubit 2 Let Ops = [exp ([PauliX, PauliY], 0,5, _), ApplyToFirstQubitA (X, _)]; permitir índices = [[0, 1], [2]]; ApplySeriesOfOpsA (Ops, índices, qubitArray);</span><span class="sxs-lookup"><span data-stu-id="2c123-121">// The following applies Exp([PauliX, PauliY], 0.5) to qubits 0, 1 // then X to qubit 2 let ops = [Exp([PauliX, PauliY], 0.5, _), ApplyToFirstQubitA(X, _)]; let indices = [[0, 1], [2]]; ApplySeriesOfOpsA(ops, indices, qubitArray);</span></span>

## <a name="see-also"></a><span data-ttu-id="2c123-122">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="2c123-122">See Also</span></span>

- [<span data-ttu-id="2c123-123">Microsoft. Quantum. Canon. ApplyOpRepeatedlyOver</span><span class="sxs-lookup"><span data-stu-id="2c123-123">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)