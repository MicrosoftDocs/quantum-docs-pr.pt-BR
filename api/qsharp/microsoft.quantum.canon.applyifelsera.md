---
uid: Microsoft.Quantum.Canon.ApplyIfElseRA
title: Operação ApplyIfElseRA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseRA
qsharp.summary: Applies one of two adjointable operations, depending on the value of a classical result.
ms.openlocfilehash: 3ebd09b1e5876ff397f3524ba828ba26a271e91e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218590"
---
# <a name="applyifelsera-operation"></a><span data-ttu-id="4ee4d-102">Operação ApplyIfElseRA</span><span class="sxs-lookup"><span data-stu-id="4ee4d-102">ApplyIfElseRA operation</span></span>

<span data-ttu-id="4ee4d-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="4ee4d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="4ee4d-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4ee4d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4ee4d-105">Aplica uma das duas operações de adjointable, dependendo do valor de um resultado clássico.</span><span class="sxs-lookup"><span data-stu-id="4ee4d-105">Applies one of two adjointable operations, depending on the value of a classical result.</span></span>

```qsharp
operation ApplyIfElseRA<'T, 'U> (result : Result, (zeroOp : ('T => Unit is Adj), zeroInput : 'T), (oneOp : ('U => Unit is Adj), oneInput : 'U)) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="4ee4d-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="4ee4d-106">Description</span></span>

<span data-ttu-id="4ee4d-107">Dado um resultado `result` , o aplica a operação `zeroOp` com `zeroInput` como sua entrada quando `result` é igual a `Zero` e se aplica `oneOp(oneInput)` quando `result == One` .</span><span class="sxs-lookup"><span data-stu-id="4ee4d-107">Given a result `result`, applies the operation `zeroOp` with `zeroInput` as its input when `result` is equal to `Zero`, and applies `oneOp(oneInput)` when `result == One`.</span></span>

## <a name="input"></a><span data-ttu-id="4ee4d-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="4ee4d-108">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="4ee4d-109">resultado: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="4ee4d-109">result : __invalid<Result>__</span></span>

<span data-ttu-id="4ee4d-110">O resultado da medida usado para determinar se `zeroOp` ou `oneOp` é aplicado.</span><span class="sxs-lookup"><span data-stu-id="4ee4d-110">The measurement result used to determine if `zeroOp` or `oneOp` is applied.</span></span>


### <a name="zeroop--t--unit--is-adj"></a><span data-ttu-id="4ee4d-111">zeroOp: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="4ee4d-111">zeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="4ee4d-112">A operação de jointable a ser aplicada quando `result == Zero` .</span><span class="sxs-lookup"><span data-stu-id="4ee4d-112">The adjointable operation to be applied when `result == Zero`.</span></span>


### <a name="zeroinput--t"></a><span data-ttu-id="4ee4d-113">zeroInput: ' t</span><span class="sxs-lookup"><span data-stu-id="4ee4d-113">zeroInput : 'T</span></span>

<span data-ttu-id="4ee4d-114">A entrada a ser fornecida a `zeroOp` quando `result == Zero` .</span><span class="sxs-lookup"><span data-stu-id="4ee4d-114">The input to be provided to `zeroOp` when `result == Zero`.</span></span>


### <a name="oneop--u--unit--is-adj"></a><span data-ttu-id="4ee4d-115">oneOp: ' U = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="4ee4d-115">oneOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="4ee4d-116">A operação de jointable a ser aplicada quando `result == One` .</span><span class="sxs-lookup"><span data-stu-id="4ee4d-116">The adjointable operation to be applied when `result == One`.</span></span>


### <a name="oneinput--u"></a><span data-ttu-id="4ee4d-117">oneInput: ' U</span><span class="sxs-lookup"><span data-stu-id="4ee4d-117">oneInput : 'U</span></span>

<span data-ttu-id="4ee4d-118">A entrada a ser fornecida a `oneOp` quando `result == One` .</span><span class="sxs-lookup"><span data-stu-id="4ee4d-118">The input to be provided to `oneOp` when `result == One`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4ee4d-119">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4ee4d-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="4ee4d-120">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="4ee4d-120">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4ee4d-121">T'</span><span class="sxs-lookup"><span data-stu-id="4ee4d-121">'T</span></span>

<span data-ttu-id="4ee4d-122">O tipo de entrada da operação `zeroOp` a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="4ee4d-122">The input type of the operation `zeroOp` to be conditionally applied.</span></span>
### <a name="u"></a><span data-ttu-id="4ee4d-123">' U</span><span class="sxs-lookup"><span data-stu-id="4ee4d-123">'U</span></span>

<span data-ttu-id="4ee4d-124">O tipo de entrada da operação `oneOp` a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="4ee4d-124">The input type of the operation `oneOp` to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="4ee4d-125">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="4ee4d-125">See Also</span></span>

- [<span data-ttu-id="4ee4d-126">Microsoft. Quantum. Canon. ApplyIfZero</span><span class="sxs-lookup"><span data-stu-id="4ee4d-126">Microsoft.Quantum.Canon.ApplyIfZero</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [<span data-ttu-id="4ee4d-127">Microsoft. Quantum. Canon. ApplyIfOne</span><span class="sxs-lookup"><span data-stu-id="4ee4d-127">Microsoft.Quantum.Canon.ApplyIfOne</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [<span data-ttu-id="4ee4d-128">Microsoft. Quantum. Canon. ApplyIfElseRC</span><span class="sxs-lookup"><span data-stu-id="4ee4d-128">Microsoft.Quantum.Canon.ApplyIfElseRC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [<span data-ttu-id="4ee4d-129">Microsoft. Quantum. Canon. ApplyIfElseRA</span><span class="sxs-lookup"><span data-stu-id="4ee4d-129">Microsoft.Quantum.Canon.ApplyIfElseRA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [<span data-ttu-id="4ee4d-130">Microsoft. Quantum. Canon. ApplyIfElseRCA</span><span class="sxs-lookup"><span data-stu-id="4ee4d-130">Microsoft.Quantum.Canon.ApplyIfElseRCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)