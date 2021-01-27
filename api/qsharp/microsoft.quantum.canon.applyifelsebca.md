---
uid: Microsoft.Quantum.Canon.ApplyIfElseBCA
title: Operação ApplyIfElseBCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseBCA
qsharp.summary: Applies one of two unitary operations, depending on the value of a classical bit.
ms.openlocfilehash: 3ed9d7cbf277f4c3acd0e6c3b5f920c3e140855d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844966"
---
# <a name="applyifelsebca-operation"></a><span data-ttu-id="d7ea6-102">Operação ApplyIfElseBCA</span><span class="sxs-lookup"><span data-stu-id="d7ea6-102">ApplyIfElseBCA operation</span></span>

<span data-ttu-id="d7ea6-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d7ea6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d7ea6-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d7ea6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d7ea6-105">Aplica uma das duas operações de unitário, dependendo do valor de um bit clássico.</span><span class="sxs-lookup"><span data-stu-id="d7ea6-105">Applies one of two unitary operations, depending on the value of a classical bit.</span></span>

```qsharp
operation ApplyIfElseBCA<'T, 'U> (bit : Bool, (trueOp : ('T => Unit is Adj + Ctl), trueInput : 'T), (falseOp : ('U => Unit is Adj + Ctl), falseInput : 'U)) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="d7ea6-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7ea6-106">Description</span></span>

<span data-ttu-id="d7ea6-107">Dado um pouco `bit` , o aplica a operação `trueOp` com `trueInput` como sua entrada quando `bit` está `true` e se aplica `falseOp(falseInput)` quando `bit` é `false` .</span><span class="sxs-lookup"><span data-stu-id="d7ea6-107">Given a bit `bit`, applies the operation `trueOp` with `trueInput` as its input when `bit` is `true`, and applies `falseOp(falseInput)` when `bit` is `false`.</span></span>

## <a name="input"></a><span data-ttu-id="d7ea6-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="d7ea6-108">Input</span></span>

### <a name="bit--bool"></a><span data-ttu-id="d7ea6-109">bit: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="d7ea6-109">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="d7ea6-110">O valor booliano usado para determinar se `trueOp` ou `falseOp` é aplicado.</span><span class="sxs-lookup"><span data-stu-id="d7ea6-110">The boolean value used to determine whether `trueOp` or `falseOp` is applied.</span></span>


### <a name="trueop--t--unit--is-adj--ctl"></a><span data-ttu-id="d7ea6-111">trueOp: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="d7ea6-111">trueOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="d7ea6-112">A operação unitário a ser aplicada quando `bit` é `true` .</span><span class="sxs-lookup"><span data-stu-id="d7ea6-112">The unitary operation to be applied when `bit` is `true`.</span></span>


### <a name="trueinput--t"></a><span data-ttu-id="d7ea6-113">trueInput: ' t</span><span class="sxs-lookup"><span data-stu-id="d7ea6-113">trueInput : 'T</span></span>

<span data-ttu-id="d7ea6-114">A entrada a ser fornecida para `trueOp` quando `bit` é `true` .</span><span class="sxs-lookup"><span data-stu-id="d7ea6-114">The input to be provided to `trueOp` when `bit` is `true`.</span></span>


### <a name="falseop--u--unit--is-adj--ctl"></a><span data-ttu-id="d7ea6-115">falseOp: ' U => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="d7ea6-115">falseOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="d7ea6-116">A operação unitário a ser aplicada quando `bit` é `false` .</span><span class="sxs-lookup"><span data-stu-id="d7ea6-116">The unitary operation to be applied when `bit` is `false`.</span></span>


### <a name="falseinput--u"></a><span data-ttu-id="d7ea6-117">falseInput: ' U</span><span class="sxs-lookup"><span data-stu-id="d7ea6-117">falseInput : 'U</span></span>

<span data-ttu-id="d7ea6-118">A entrada a ser fornecida para `falseOp` quando `bit` é `false` .</span><span class="sxs-lookup"><span data-stu-id="d7ea6-118">The input to be provided to `falseOp` when `bit` is `false`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d7ea6-119">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d7ea6-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d7ea6-120">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="d7ea6-120">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d7ea6-121">T'</span><span class="sxs-lookup"><span data-stu-id="d7ea6-121">'T</span></span>

<span data-ttu-id="d7ea6-122">O tipo de entrada da operação `trueOp` a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="d7ea6-122">The input type of the operation `trueOp` to be conditionally applied.</span></span>
### <a name="u"></a><span data-ttu-id="d7ea6-123">' U</span><span class="sxs-lookup"><span data-stu-id="d7ea6-123">'U</span></span>

<span data-ttu-id="d7ea6-124">O tipo de entrada da operação `falseOp` a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="d7ea6-124">The input type of the operation `falseOp` to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="d7ea6-125">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d7ea6-125">See Also</span></span>

- [<span data-ttu-id="d7ea6-126">Microsoft. Quantum. Canon. ApplyIfZero</span><span class="sxs-lookup"><span data-stu-id="d7ea6-126">Microsoft.Quantum.Canon.ApplyIfZero</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [<span data-ttu-id="d7ea6-127">Microsoft. Quantum. Canon. ApplyIfOne</span><span class="sxs-lookup"><span data-stu-id="d7ea6-127">Microsoft.Quantum.Canon.ApplyIfOne</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [<span data-ttu-id="d7ea6-128">Microsoft. Quantum. Canon. ApplyIfElseRC</span><span class="sxs-lookup"><span data-stu-id="d7ea6-128">Microsoft.Quantum.Canon.ApplyIfElseRC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [<span data-ttu-id="d7ea6-129">Microsoft. Quantum. Canon. ApplyIfElseRA</span><span class="sxs-lookup"><span data-stu-id="d7ea6-129">Microsoft.Quantum.Canon.ApplyIfElseRA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [<span data-ttu-id="d7ea6-130">Microsoft. Quantum. Canon. ApplyIfElseRCA</span><span class="sxs-lookup"><span data-stu-id="d7ea6-130">Microsoft.Quantum.Canon.ApplyIfElseRCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)