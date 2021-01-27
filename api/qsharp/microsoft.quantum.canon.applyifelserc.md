---
uid: Microsoft.Quantum.Canon.ApplyIfElseRC
title: Operação ApplyIfElseRC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseRC
qsharp.summary: Applies one of two controllable operations, depending on the value of a classical result.
ms.openlocfilehash: bac763168dbc7379691f850a79cbb6e61639ba89
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841782"
---
# <a name="applyifelserc-operation"></a><span data-ttu-id="4fc3f-102">Operação ApplyIfElseRC</span><span class="sxs-lookup"><span data-stu-id="4fc3f-102">ApplyIfElseRC operation</span></span>

<span data-ttu-id="4fc3f-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="4fc3f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="4fc3f-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4fc3f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4fc3f-105">Aplica uma das duas operações controláveis, dependendo do valor de um resultado clássico.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-105">Applies one of two controllable operations, depending on the value of a classical result.</span></span>

```qsharp
operation ApplyIfElseRC<'T, 'U> (result : Result, (zeroOp : ('T => Unit is Ctl), zeroInput : 'T), (oneOp : ('U => Unit is Ctl), oneInput : 'U)) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="4fc3f-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="4fc3f-106">Description</span></span>

<span data-ttu-id="4fc3f-107">Dado um resultado `result` , o aplica a operação `zeroOp` com `zeroInput` como sua entrada quando `result` é igual a `Zero` e se aplica `oneOp(oneInput)` quando `result == One` .</span><span class="sxs-lookup"><span data-stu-id="4fc3f-107">Given a result `result`, applies the operation `zeroOp` with `zeroInput` as its input when `result` is equal to `Zero`, and applies `oneOp(oneInput)` when `result == One`.</span></span>

## <a name="input"></a><span data-ttu-id="4fc3f-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="4fc3f-108">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="4fc3f-109">resultado: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="4fc3f-109">result : __invalid<Result>__</span></span>

<span data-ttu-id="4fc3f-110">O resultado da medida usado para determinar se `zeroOp` ou `oneOp` é aplicado.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-110">The measurement result used to determine if `zeroOp` or `oneOp` is applied.</span></span>


### <a name="zeroop--t--unit--is-ctl"></a><span data-ttu-id="4fc3f-111">zeroOp: T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é CTL</span><span class="sxs-lookup"><span data-stu-id="4fc3f-111">zeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="4fc3f-112">A operação controláveis a ser aplicada quando `result == Zero` .</span><span class="sxs-lookup"><span data-stu-id="4fc3f-112">The controllable operation to be applied when `result == Zero`.</span></span>


### <a name="zeroinput--t"></a><span data-ttu-id="4fc3f-113">zeroInput: ' t</span><span class="sxs-lookup"><span data-stu-id="4fc3f-113">zeroInput : 'T</span></span>

<span data-ttu-id="4fc3f-114">A entrada a ser fornecida a `zeroOp` quando `result == Zero` .</span><span class="sxs-lookup"><span data-stu-id="4fc3f-114">The input to be provided to `zeroOp` when `result == Zero`.</span></span>


### <a name="oneop--u--unit--is-ctl"></a><span data-ttu-id="4fc3f-115">oneOp: ' U => [unidade](xref:microsoft.quantum.lang-ref.unit)  é CTL</span><span class="sxs-lookup"><span data-stu-id="4fc3f-115">oneOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="4fc3f-116">A operação controláveis a ser aplicada quando `result == One` .</span><span class="sxs-lookup"><span data-stu-id="4fc3f-116">The controllable operation to be applied when `result == One`.</span></span>


### <a name="oneinput--u"></a><span data-ttu-id="4fc3f-117">oneInput: ' U</span><span class="sxs-lookup"><span data-stu-id="4fc3f-117">oneInput : 'U</span></span>

<span data-ttu-id="4fc3f-118">A entrada a ser fornecida a `oneOp` quando `result == One` .</span><span class="sxs-lookup"><span data-stu-id="4fc3f-118">The input to be provided to `oneOp` when `result == One`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4fc3f-119">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4fc3f-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="4fc3f-120">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="4fc3f-120">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4fc3f-121">T'</span><span class="sxs-lookup"><span data-stu-id="4fc3f-121">'T</span></span>

<span data-ttu-id="4fc3f-122">O tipo de entrada da operação `zeroOp` a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-122">The input type of the operation `zeroOp` to be conditionally applied.</span></span>
### <a name="u"></a><span data-ttu-id="4fc3f-123">' U</span><span class="sxs-lookup"><span data-stu-id="4fc3f-123">'U</span></span>

<span data-ttu-id="4fc3f-124">O tipo de entrada da operação `oneOp` a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-124">The input type of the operation `oneOp` to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="4fc3f-125">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="4fc3f-125">See Also</span></span>

- [<span data-ttu-id="4fc3f-126">Microsoft. Quantum. Canon. ApplyIfZero</span><span class="sxs-lookup"><span data-stu-id="4fc3f-126">Microsoft.Quantum.Canon.ApplyIfZero</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [<span data-ttu-id="4fc3f-127">Microsoft. Quantum. Canon. ApplyIfOne</span><span class="sxs-lookup"><span data-stu-id="4fc3f-127">Microsoft.Quantum.Canon.ApplyIfOne</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [<span data-ttu-id="4fc3f-128">Microsoft. Quantum. Canon. ApplyIfElseRC</span><span class="sxs-lookup"><span data-stu-id="4fc3f-128">Microsoft.Quantum.Canon.ApplyIfElseRC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [<span data-ttu-id="4fc3f-129">Microsoft. Quantum. Canon. ApplyIfElseRA</span><span class="sxs-lookup"><span data-stu-id="4fc3f-129">Microsoft.Quantum.Canon.ApplyIfElseRA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [<span data-ttu-id="4fc3f-130">Microsoft. Quantum. Canon. ApplyIfElseRCA</span><span class="sxs-lookup"><span data-stu-id="4fc3f-130">Microsoft.Quantum.Canon.ApplyIfElseRCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)