---
uid: Microsoft.Quantum.Canon.ApplyIfElseRCA
title: Operação ApplyIfElseRCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseRCA
qsharp.summary: Applies one of two unitary operations, depending on the value of a classical result.
ms.openlocfilehash: 6dfa2a5cf88029ac772b09bc2d36a5f19ef37a14
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844944"
---
# <a name="applyifelserca-operation"></a><span data-ttu-id="3618a-102">Operação ApplyIfElseRCA</span><span class="sxs-lookup"><span data-stu-id="3618a-102">ApplyIfElseRCA operation</span></span>

<span data-ttu-id="3618a-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="3618a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="3618a-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3618a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3618a-105">Aplica uma das duas operações de unitário, dependendo do valor de um resultado clássico.</span><span class="sxs-lookup"><span data-stu-id="3618a-105">Applies one of two unitary operations, depending on the value of a classical result.</span></span>

```qsharp
operation ApplyIfElseRCA<'T, 'U> (result : Result, (zeroOp : ('T => Unit is Adj + Ctl), zeroInput : 'T), (oneOp : ('U => Unit is Adj + Ctl), oneInput : 'U)) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="3618a-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="3618a-106">Description</span></span>

<span data-ttu-id="3618a-107">Dado um resultado `result` , o aplica a operação `zeroOp` com `zeroInput` como sua entrada quando `result` é igual a `Zero` e se aplica `oneOp(oneInput)` quando `result == One` .</span><span class="sxs-lookup"><span data-stu-id="3618a-107">Given a result `result`, applies the operation `zeroOp` with `zeroInput` as its input when `result` is equal to `Zero`, and applies `oneOp(oneInput)` when `result == One`.</span></span>

## <a name="input"></a><span data-ttu-id="3618a-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="3618a-108">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="3618a-109">resultado: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="3618a-109">result : __invalid<Result>__</span></span>

<span data-ttu-id="3618a-110">O resultado da medida usado para determinar se `zeroOp` ou `oneOp` é aplicado.</span><span class="sxs-lookup"><span data-stu-id="3618a-110">The measurement result used to determine if `zeroOp` or `oneOp` is applied.</span></span>


### <a name="zeroop--t--unit--is-adj--ctl"></a><span data-ttu-id="3618a-111">zeroOp: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="3618a-111">zeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="3618a-112">A operação unitário a ser aplicada quando `result == Zero` .</span><span class="sxs-lookup"><span data-stu-id="3618a-112">The unitary operation to be applied when `result == Zero`.</span></span>


### <a name="zeroinput--t"></a><span data-ttu-id="3618a-113">zeroInput: ' t</span><span class="sxs-lookup"><span data-stu-id="3618a-113">zeroInput : 'T</span></span>

<span data-ttu-id="3618a-114">A entrada a ser fornecida a `zeroOp` quando `result == Zero` .</span><span class="sxs-lookup"><span data-stu-id="3618a-114">The input to be provided to `zeroOp` when `result == Zero`.</span></span>


### <a name="oneop--u--unit--is-adj--ctl"></a><span data-ttu-id="3618a-115">oneOp: ' U => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="3618a-115">oneOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="3618a-116">A operação unitário a ser aplicada quando `result == One` .</span><span class="sxs-lookup"><span data-stu-id="3618a-116">The unitary operation to be applied when `result == One`.</span></span>


### <a name="oneinput--u"></a><span data-ttu-id="3618a-117">oneInput: ' U</span><span class="sxs-lookup"><span data-stu-id="3618a-117">oneInput : 'U</span></span>

<span data-ttu-id="3618a-118">A entrada a ser fornecida a `oneOp` quando `result == One` .</span><span class="sxs-lookup"><span data-stu-id="3618a-118">The input to be provided to `oneOp` when `result == One`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3618a-119">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3618a-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="3618a-120">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="3618a-120">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3618a-121">T'</span><span class="sxs-lookup"><span data-stu-id="3618a-121">'T</span></span>

<span data-ttu-id="3618a-122">O tipo de entrada da operação `zeroOp` a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="3618a-122">The input type of the operation `zeroOp` to be conditionally applied.</span></span>
### <a name="u"></a><span data-ttu-id="3618a-123">' U</span><span class="sxs-lookup"><span data-stu-id="3618a-123">'U</span></span>

<span data-ttu-id="3618a-124">O tipo de entrada da operação `oneOp` a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="3618a-124">The input type of the operation `oneOp` to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="3618a-125">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="3618a-125">See Also</span></span>

- [<span data-ttu-id="3618a-126">Microsoft. Quantum. Canon. ApplyIfZero</span><span class="sxs-lookup"><span data-stu-id="3618a-126">Microsoft.Quantum.Canon.ApplyIfZero</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [<span data-ttu-id="3618a-127">Microsoft. Quantum. Canon. ApplyIfOne</span><span class="sxs-lookup"><span data-stu-id="3618a-127">Microsoft.Quantum.Canon.ApplyIfOne</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [<span data-ttu-id="3618a-128">Microsoft. Quantum. Canon. ApplyIfElseRC</span><span class="sxs-lookup"><span data-stu-id="3618a-128">Microsoft.Quantum.Canon.ApplyIfElseRC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [<span data-ttu-id="3618a-129">Microsoft. Quantum. Canon. ApplyIfElseRA</span><span class="sxs-lookup"><span data-stu-id="3618a-129">Microsoft.Quantum.Canon.ApplyIfElseRA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [<span data-ttu-id="3618a-130">Microsoft. Quantum. Canon. ApplyIfElseRCA</span><span class="sxs-lookup"><span data-stu-id="3618a-130">Microsoft.Quantum.Canon.ApplyIfElseRCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)