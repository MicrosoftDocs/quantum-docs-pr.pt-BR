---
uid: Microsoft.Quantum.Canon.ApplyIfC
title: Operação ApplyIfC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfC
qsharp.summary: Applies a controllable operation conditioned on a classical bit.
ms.openlocfilehash: e16254154909eb844164538acb7b82fedc11f86a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694304"
---
# <a name="applyifc-operation"></a><span data-ttu-id="adbde-102">Operação ApplyIfC</span><span class="sxs-lookup"><span data-stu-id="adbde-102">ApplyIfC operation</span></span>

<span data-ttu-id="adbde-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="adbde-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="adbde-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="adbde-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="adbde-105">Aplica uma operação controlável condicionalmente em um bit clássico.</span><span class="sxs-lookup"><span data-stu-id="adbde-105">Applies a controllable operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIfC<'T> (op : ('T => Unit is Ctl), bit : Bool, target : 'T) : Unit
```


## <a name="description"></a><span data-ttu-id="adbde-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="adbde-106">Description</span></span>

<span data-ttu-id="adbde-107">Dada uma operação `op` e um valor de bit `bit` , aplica- `op` `target` se ao If `bit` is `true` .</span><span class="sxs-lookup"><span data-stu-id="adbde-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="adbde-108">Se `false` nada acontecer com o `target` .</span><span class="sxs-lookup"><span data-stu-id="adbde-108">If `false`, nothing happens to the `target`.</span></span>
<span data-ttu-id="adbde-109">O sufixo `C` indica que a operação a ser aplicada é controlável.</span><span class="sxs-lookup"><span data-stu-id="adbde-109">The suffix `C` indicates that the operation to be applied is controllable.</span></span>

## <a name="input"></a><span data-ttu-id="adbde-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="adbde-110">Input</span></span>

### <a name="op--t--unit-ctl"></a><span data-ttu-id="adbde-111">op: ' t => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="adbde-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="adbde-112">Uma operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="adbde-112">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="adbde-113">bit: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="adbde-113">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="adbde-114">um booliano que controla se op é aplicado ou não.</span><span class="sxs-lookup"><span data-stu-id="adbde-114">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="adbde-115">destino: ' t</span><span class="sxs-lookup"><span data-stu-id="adbde-115">target : 'T</span></span>

<span data-ttu-id="adbde-116">A entrada à qual a operação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="adbde-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="adbde-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="adbde-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="adbde-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="adbde-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="adbde-119">T'</span><span class="sxs-lookup"><span data-stu-id="adbde-119">'T</span></span>

<span data-ttu-id="adbde-120">O tipo de entrada da operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="adbde-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="adbde-121">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="adbde-121">See Also</span></span>

- [<span data-ttu-id="adbde-122">Microsoft. Quantum. Canon. ApplyIfC</span><span class="sxs-lookup"><span data-stu-id="adbde-122">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="adbde-123">Microsoft. Quantum. Canon. ApplyIfA</span><span class="sxs-lookup"><span data-stu-id="adbde-123">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="adbde-124">Microsoft. Quantum. Canon. ApplyIfCA</span><span class="sxs-lookup"><span data-stu-id="adbde-124">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)