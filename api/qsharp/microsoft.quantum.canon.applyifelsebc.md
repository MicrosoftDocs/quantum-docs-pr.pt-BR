---
uid: Microsoft.Quantum.Canon.ApplyIfElseBC
title: Operação ApplyIfElseBC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseBC
qsharp.summary: Applies one of two controllable operations, depending on the value of a classical bit.
ms.openlocfilehash: 6140a8382cbd00589d1aef99e004f71f5d9295a9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841831"
---
# <a name="applyifelsebc-operation"></a><span data-ttu-id="5fab2-102">Operação ApplyIfElseBC</span><span class="sxs-lookup"><span data-stu-id="5fab2-102">ApplyIfElseBC operation</span></span>

<span data-ttu-id="5fab2-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5fab2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5fab2-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5fab2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5fab2-105">Aplica uma das duas operações controláveis, dependendo do valor de um bit clássico.</span><span class="sxs-lookup"><span data-stu-id="5fab2-105">Applies one of two controllable operations, depending on the value of a classical bit.</span></span>

```qsharp
operation ApplyIfElseBC<'T, 'U> (bit : Bool, (trueOp : ('T => Unit is Ctl), trueInput : 'T), (falseOp : ('U => Unit is Ctl), falseInput : 'U)) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="5fab2-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="5fab2-106">Description</span></span>

<span data-ttu-id="5fab2-107">Dado um pouco `bit` , o aplica a operação `trueOp` com `trueInput` como sua entrada quando `bit` está `true` e se aplica `falseOp(falseInput)` quando `bit` é `false` .</span><span class="sxs-lookup"><span data-stu-id="5fab2-107">Given a bit `bit`, applies the operation `trueOp` with `trueInput` as its input when `bit` is `true`, and applies `falseOp(falseInput)` when `bit` is `false`.</span></span>

## <a name="input"></a><span data-ttu-id="5fab2-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="5fab2-108">Input</span></span>

### <a name="bit--bool"></a><span data-ttu-id="5fab2-109">bit: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="5fab2-109">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="5fab2-110">O valor booliano usado para determinar se `trueOp` ou `falseOp` é aplicado.</span><span class="sxs-lookup"><span data-stu-id="5fab2-110">The boolean value used to determine whether `trueOp` or `falseOp` is applied.</span></span>


### <a name="trueop--t--unit--is-ctl"></a><span data-ttu-id="5fab2-111">trueOp: T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é CTL</span><span class="sxs-lookup"><span data-stu-id="5fab2-111">trueOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="5fab2-112">A operação controláveis a ser aplicada quando `bit` é `true` .</span><span class="sxs-lookup"><span data-stu-id="5fab2-112">The controllable operation to be applied when `bit` is `true`.</span></span>


### <a name="trueinput--t"></a><span data-ttu-id="5fab2-113">trueInput: ' t</span><span class="sxs-lookup"><span data-stu-id="5fab2-113">trueInput : 'T</span></span>

<span data-ttu-id="5fab2-114">A entrada a ser fornecida para `trueOp` quando `bit` é `true` .</span><span class="sxs-lookup"><span data-stu-id="5fab2-114">The input to be provided to `trueOp` when `bit` is `true`.</span></span>


### <a name="falseop--u--unit--is-ctl"></a><span data-ttu-id="5fab2-115">falseOp: ' U => [unidade](xref:microsoft.quantum.lang-ref.unit)  é CTL</span><span class="sxs-lookup"><span data-stu-id="5fab2-115">falseOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="5fab2-116">A operação controláveis a ser aplicada quando `bit` é `false` .</span><span class="sxs-lookup"><span data-stu-id="5fab2-116">The controllable operation to be applied when `bit` is `false`.</span></span>


### <a name="falseinput--u"></a><span data-ttu-id="5fab2-117">falseInput: ' U</span><span class="sxs-lookup"><span data-stu-id="5fab2-117">falseInput : 'U</span></span>

<span data-ttu-id="5fab2-118">A entrada a ser fornecida para `falseOp` quando `bit` é `false` .</span><span class="sxs-lookup"><span data-stu-id="5fab2-118">The input to be provided to `falseOp` when `bit` is `false`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5fab2-119">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5fab2-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="5fab2-120">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="5fab2-120">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5fab2-121">T'</span><span class="sxs-lookup"><span data-stu-id="5fab2-121">'T</span></span>

<span data-ttu-id="5fab2-122">O tipo de entrada da operação `trueOp` a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="5fab2-122">The input type of the operation `trueOp` to be conditionally applied.</span></span>
### <a name="u"></a><span data-ttu-id="5fab2-123">' U</span><span class="sxs-lookup"><span data-stu-id="5fab2-123">'U</span></span>

<span data-ttu-id="5fab2-124">O tipo de entrada da operação `falseOp` a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="5fab2-124">The input type of the operation `falseOp` to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="5fab2-125">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="5fab2-125">See Also</span></span>

- [<span data-ttu-id="5fab2-126">Microsoft. Quantum. Canon. ApplyIfZero</span><span class="sxs-lookup"><span data-stu-id="5fab2-126">Microsoft.Quantum.Canon.ApplyIfZero</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [<span data-ttu-id="5fab2-127">Microsoft. Quantum. Canon. ApplyIfOne</span><span class="sxs-lookup"><span data-stu-id="5fab2-127">Microsoft.Quantum.Canon.ApplyIfOne</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [<span data-ttu-id="5fab2-128">Microsoft. Quantum. Canon. ApplyIfElseRC</span><span class="sxs-lookup"><span data-stu-id="5fab2-128">Microsoft.Quantum.Canon.ApplyIfElseRC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [<span data-ttu-id="5fab2-129">Microsoft. Quantum. Canon. ApplyIfElseRA</span><span class="sxs-lookup"><span data-stu-id="5fab2-129">Microsoft.Quantum.Canon.ApplyIfElseRA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [<span data-ttu-id="5fab2-130">Microsoft. Quantum. Canon. ApplyIfElseRCA</span><span class="sxs-lookup"><span data-stu-id="5fab2-130">Microsoft.Quantum.Canon.ApplyIfElseRCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)