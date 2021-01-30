---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsC
title: Operação ApplySeriesOfOpsC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsC
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Controlled)
ms.openlocfilehash: 308256833dc607f685e3a5f2278e374cf3b6ce22
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844639"
---
# <a name="applyseriesofopsc-operation"></a><span data-ttu-id="d3147-102">Operação ApplySeriesOfOpsC</span><span class="sxs-lookup"><span data-stu-id="d3147-102">ApplySeriesOfOpsC operation</span></span>

<span data-ttu-id="d3147-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d3147-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d3147-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d3147-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d3147-105">Aplica uma lista de operações e seus destinos seqüencialmente em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="d3147-105">Applies a list of ops and their targets sequentially on an array.</span></span> <span data-ttu-id="d3147-106">Controlado</span><span class="sxs-lookup"><span data-stu-id="d3147-106">(Controlled)</span></span>

```qsharp
operation ApplySeriesOfOpsC<'T> (listOfOps : ('T[] => Unit is Ctl)[], targets : Int[][], register : 'T[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="d3147-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="d3147-107">Input</span></span>

### <a name="listofops--t--unit--is-ctl"></a><span data-ttu-id="d3147-108">listOfOps: t [] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é CTL []</span><span class="sxs-lookup"><span data-stu-id="d3147-108">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl[]</span></span>

<span data-ttu-id="d3147-109">Lista de operações, cada uma levando uma matriz não, a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="d3147-109">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="d3147-110">Eles são aplicados em sequência, o índice mais baixo primeiro.</span><span class="sxs-lookup"><span data-stu-id="d3147-110">They are applied sequentially, lowest index first.</span></span>
<span data-ttu-id="d3147-111">Cada um deve ter um functor controlado</span><span class="sxs-lookup"><span data-stu-id="d3147-111">Each must have a Controlled functor</span></span>


### <a name="targets--int"></a><span data-ttu-id="d3147-112">destinos: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="d3147-112">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="d3147-113">Matrizes aninhadas que descrevem os destinos da operação.</span><span class="sxs-lookup"><span data-stu-id="d3147-113">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="d3147-114">Cada matriz deve conter uma lista de ints descrevendo os índices a serem usados.</span><span class="sxs-lookup"><span data-stu-id="d3147-114">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="d3147-115">registrar: t []</span><span class="sxs-lookup"><span data-stu-id="d3147-115">register : 'T[]</span></span>

<span data-ttu-id="d3147-116">Qubit registrar-se para ser tratado.</span><span class="sxs-lookup"><span data-stu-id="d3147-116">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d3147-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d3147-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d3147-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="d3147-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d3147-119">T'</span><span class="sxs-lookup"><span data-stu-id="d3147-119">'T</span></span>



## <a name="example"></a><span data-ttu-id="d3147-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d3147-120">Example</span></span>

<span data-ttu-id="d3147-121">O seguinte aplica-se exp ([PauliX, PauliY], 0,5) a qubits 0, 1//then X para qubit 2 Let Ops = [exp ([PauliX, PauliY], 0,5, _), ApplyToFirstQubitC (X, _)]; permitir índices = [[0, 1], [2]]; ApplySeriesOfOpsC (Ops, índices, qubitArray);</span><span class="sxs-lookup"><span data-stu-id="d3147-121">// The following applies Exp([PauliX, PauliY], 0.5) to qubits 0, 1 // then X to qubit 2 let ops = [Exp([PauliX, PauliY], 0.5, _), ApplyToFirstQubitC(X, _)]; let indices = [[0, 1], [2]]; ApplySeriesOfOpsC(ops, indices, qubitArray);</span></span>

## <a name="see-also"></a><span data-ttu-id="d3147-122">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d3147-122">See Also</span></span>

- [<span data-ttu-id="d3147-123">Microsoft. Quantum. Canon. ApplyOpRepeatedlyOver</span><span class="sxs-lookup"><span data-stu-id="d3147-123">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)