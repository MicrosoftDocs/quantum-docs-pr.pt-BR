---
uid: Microsoft.Quantum.Canon.ApplyIfElseB
title: Operação ApplyIfElseB
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseB
qsharp.summary: Applies one of two operations, depending on the value of a classical bit.
ms.openlocfilehash: 68c06a5141b9ff423c2d18adc3a9e162eed939f6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694301"
---
# <a name="applyifelseb-operation"></a><span data-ttu-id="8a9dc-102">Operação ApplyIfElseB</span><span class="sxs-lookup"><span data-stu-id="8a9dc-102">ApplyIfElseB operation</span></span>

<span data-ttu-id="8a9dc-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8a9dc-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8a9dc-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8a9dc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8a9dc-105">Aplica uma das duas operações, dependendo do valor de um bit clássico.</span><span class="sxs-lookup"><span data-stu-id="8a9dc-105">Applies one of two operations, depending on the value of a classical bit.</span></span>

```qsharp
operation ApplyIfElseB<'T, 'U> (bit : Bool, (trueOp : ('T => Unit), trueInput : 'T), (falseOp : ('U => Unit), falseInput : 'U)) : Unit
```


## <a name="description"></a><span data-ttu-id="8a9dc-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a9dc-106">Description</span></span>

<span data-ttu-id="8a9dc-107">Dado um pouco `bit` , o aplica a operação `trueOp` com `trueInput` como sua entrada quando `bit` está `true` e se aplica `falseOp(falseInput)` quando `bit` é `false` .</span><span class="sxs-lookup"><span data-stu-id="8a9dc-107">Given a bit `bit`, applies the operation `trueOp` with `trueInput` as its input when `bit` is `true`, and applies `falseOp(falseInput)` when `bit` is `false`.</span></span>

## <a name="input"></a><span data-ttu-id="8a9dc-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a9dc-108">Input</span></span>

### <a name="bit--bool"></a><span data-ttu-id="8a9dc-109">bit: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="8a9dc-109">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="8a9dc-110">O valor booliano usado para determinar se `trueOp` ou `falseOp` é aplicado.</span><span class="sxs-lookup"><span data-stu-id="8a9dc-110">The boolean value used to determine whether `trueOp` or `falseOp` is applied.</span></span>


### <a name="trueop--t--unit"></a><span data-ttu-id="8a9dc-111">trueOp: t = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="8a9dc-111">trueOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="8a9dc-112">A operação a ser aplicada quando `bit` é `true` .</span><span class="sxs-lookup"><span data-stu-id="8a9dc-112">The operation to be applied when `bit` is `true`.</span></span>


### <a name="trueinput--t"></a><span data-ttu-id="8a9dc-113">trueInput: ' t</span><span class="sxs-lookup"><span data-stu-id="8a9dc-113">trueInput : 'T</span></span>

<span data-ttu-id="8a9dc-114">A entrada a ser fornecida para `trueOp` quando `bit` é `true` .</span><span class="sxs-lookup"><span data-stu-id="8a9dc-114">The input to be provided to `trueOp` when `bit` is `true`.</span></span>


### <a name="falseop--u--unit"></a><span data-ttu-id="8a9dc-115">falseOp: ' U = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="8a9dc-115">falseOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="8a9dc-116">A operação a ser aplicada quando `bit` é `false` .</span><span class="sxs-lookup"><span data-stu-id="8a9dc-116">The operation to be applied when `bit` is `false`.</span></span>


### <a name="falseinput--u"></a><span data-ttu-id="8a9dc-117">falseInput: ' U</span><span class="sxs-lookup"><span data-stu-id="8a9dc-117">falseInput : 'U</span></span>

<span data-ttu-id="8a9dc-118">A entrada a ser fornecida para `falseOp` quando `bit` é `false` .</span><span class="sxs-lookup"><span data-stu-id="8a9dc-118">The input to be provided to `falseOp` when `bit` is `false`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8a9dc-119">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8a9dc-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="8a9dc-120">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="8a9dc-120">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8a9dc-121">T'</span><span class="sxs-lookup"><span data-stu-id="8a9dc-121">'T</span></span>

<span data-ttu-id="8a9dc-122">O tipo de entrada da operação `trueOp` a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="8a9dc-122">The input type of the operation `trueOp` to be conditionally applied.</span></span>
### <a name="u"></a><span data-ttu-id="8a9dc-123">' U</span><span class="sxs-lookup"><span data-stu-id="8a9dc-123">'U</span></span>

<span data-ttu-id="8a9dc-124">O tipo de entrada da operação `falseOp` a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="8a9dc-124">The input type of the operation `falseOp` to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="8a9dc-125">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="8a9dc-125">See Also</span></span>

- [<span data-ttu-id="8a9dc-126">Microsoft. Quantum. Canon. ApplyIfZero</span><span class="sxs-lookup"><span data-stu-id="8a9dc-126">Microsoft.Quantum.Canon.ApplyIfZero</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [<span data-ttu-id="8a9dc-127">Microsoft. Quantum. Canon. ApplyIfOne</span><span class="sxs-lookup"><span data-stu-id="8a9dc-127">Microsoft.Quantum.Canon.ApplyIfOne</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [<span data-ttu-id="8a9dc-128">Microsoft. Quantum. Canon. ApplyIfElseRC</span><span class="sxs-lookup"><span data-stu-id="8a9dc-128">Microsoft.Quantum.Canon.ApplyIfElseRC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [<span data-ttu-id="8a9dc-129">Microsoft. Quantum. Canon. ApplyIfElseRA</span><span class="sxs-lookup"><span data-stu-id="8a9dc-129">Microsoft.Quantum.Canon.ApplyIfElseRA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [<span data-ttu-id="8a9dc-130">Microsoft. Quantum. Canon. ApplyIfElseRCA</span><span class="sxs-lookup"><span data-stu-id="8a9dc-130">Microsoft.Quantum.Canon.ApplyIfElseRCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)