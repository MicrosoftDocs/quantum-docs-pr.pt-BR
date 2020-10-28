---
uid: Microsoft.Quantum.Canon.ApplyIfElseRCA
title: Operação ApplyIfElseRCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseRCA
qsharp.summary: Applies one of two unitary operations, depending on the value of a classical result.
ms.openlocfilehash: c48d75323f036ebce1a316382a05cd2578db47a3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694285"
---
# <a name="applyifelserca-operation"></a><span data-ttu-id="aeb54-102">Operação ApplyIfElseRCA</span><span class="sxs-lookup"><span data-stu-id="aeb54-102">ApplyIfElseRCA operation</span></span>

<span data-ttu-id="aeb54-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="aeb54-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="aeb54-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="aeb54-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="aeb54-105">Aplica uma das duas operações de unitário, dependendo do valor de um resultado clássico.</span><span class="sxs-lookup"><span data-stu-id="aeb54-105">Applies one of two unitary operations, depending on the value of a classical result.</span></span>

```qsharp
operation ApplyIfElseRCA<'T, 'U> (result : Result, (zeroOp : ('T => Unit is Adj + Ctl), zeroInput : 'T), (oneOp : ('U => Unit is Adj + Ctl), oneInput : 'U)) : Unit
```


## <a name="description"></a><span data-ttu-id="aeb54-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="aeb54-106">Description</span></span>

<span data-ttu-id="aeb54-107">Dado um resultado `result` , o aplica a operação `zeroOp` com `zeroInput` como sua entrada quando `result` é igual a `Zero` e se aplica `oneOp(oneInput)` quando `result == One` .</span><span class="sxs-lookup"><span data-stu-id="aeb54-107">Given a result `result`, applies the operation `zeroOp` with `zeroInput` as its input when `result` is equal to `Zero`, and applies `oneOp(oneInput)` when `result == One`.</span></span>

## <a name="input"></a><span data-ttu-id="aeb54-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="aeb54-108">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="aeb54-109">resultado: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="aeb54-109">result : __invalid<Result>__</span></span>

<span data-ttu-id="aeb54-110">O resultado da medida usado para determinar se `zeroOp` ou `oneOp` é aplicado.</span><span class="sxs-lookup"><span data-stu-id="aeb54-110">The measurement result used to determine if `zeroOp` or `oneOp` is applied.</span></span>


### <a name="zeroop--t--unit-adj--ctl"></a><span data-ttu-id="aeb54-111">zeroOp: t => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL</span><span class="sxs-lookup"><span data-stu-id="aeb54-111">zeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="aeb54-112">A operação unitário a ser aplicada quando `result == Zero` .</span><span class="sxs-lookup"><span data-stu-id="aeb54-112">The unitary operation to be applied when `result == Zero`.</span></span>


### <a name="zeroinput--t"></a><span data-ttu-id="aeb54-113">zeroInput: ' t</span><span class="sxs-lookup"><span data-stu-id="aeb54-113">zeroInput : 'T</span></span>

<span data-ttu-id="aeb54-114">A entrada a ser fornecida a `zeroOp` quando `result == Zero` .</span><span class="sxs-lookup"><span data-stu-id="aeb54-114">The input to be provided to `zeroOp` when `result == Zero`.</span></span>


### <a name="oneop--u--unit-adj--ctl"></a><span data-ttu-id="aeb54-115">oneOp: ' U => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL</span><span class="sxs-lookup"><span data-stu-id="aeb54-115">oneOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="aeb54-116">A operação unitário a ser aplicada quando `result == One` .</span><span class="sxs-lookup"><span data-stu-id="aeb54-116">The unitary operation to be applied when `result == One`.</span></span>


### <a name="oneinput--u"></a><span data-ttu-id="aeb54-117">oneInput: ' U</span><span class="sxs-lookup"><span data-stu-id="aeb54-117">oneInput : 'U</span></span>

<span data-ttu-id="aeb54-118">A entrada a ser fornecida a `oneOp` quando `result == One` .</span><span class="sxs-lookup"><span data-stu-id="aeb54-118">The input to be provided to `oneOp` when `result == One`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="aeb54-119">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="aeb54-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="aeb54-120">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="aeb54-120">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="aeb54-121">T'</span><span class="sxs-lookup"><span data-stu-id="aeb54-121">'T</span></span>

<span data-ttu-id="aeb54-122">O tipo de entrada da operação `zeroOp` a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="aeb54-122">The input type of the operation `zeroOp` to be conditionally applied.</span></span>
### <a name="u"></a><span data-ttu-id="aeb54-123">' U</span><span class="sxs-lookup"><span data-stu-id="aeb54-123">'U</span></span>

<span data-ttu-id="aeb54-124">O tipo de entrada da operação `oneOp` a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="aeb54-124">The input type of the operation `oneOp` to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="aeb54-125">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="aeb54-125">See Also</span></span>

- [<span data-ttu-id="aeb54-126">Microsoft. Quantum. Canon. ApplyIfZero</span><span class="sxs-lookup"><span data-stu-id="aeb54-126">Microsoft.Quantum.Canon.ApplyIfZero</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [<span data-ttu-id="aeb54-127">Microsoft. Quantum. Canon. ApplyIfOne</span><span class="sxs-lookup"><span data-stu-id="aeb54-127">Microsoft.Quantum.Canon.ApplyIfOne</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [<span data-ttu-id="aeb54-128">Microsoft. Quantum. Canon. ApplyIfElseRC</span><span class="sxs-lookup"><span data-stu-id="aeb54-128">Microsoft.Quantum.Canon.ApplyIfElseRC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [<span data-ttu-id="aeb54-129">Microsoft. Quantum. Canon. ApplyIfElseRA</span><span class="sxs-lookup"><span data-stu-id="aeb54-129">Microsoft.Quantum.Canon.ApplyIfElseRA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [<span data-ttu-id="aeb54-130">Microsoft. Quantum. Canon. ApplyIfElseRCA</span><span class="sxs-lookup"><span data-stu-id="aeb54-130">Microsoft.Quantum.Canon.ApplyIfElseRCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)