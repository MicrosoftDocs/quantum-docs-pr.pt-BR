---
uid: Microsoft.Quantum.Canon.ApplyIfC
title: Operação ApplyIfC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfC
qsharp.summary: Applies a controllable operation conditioned on a classical bit.
ms.openlocfilehash: 35430cb7cf491965b7b69ace6d3f41599dbadd51
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218709"
---
# <a name="applyifc-operation"></a><span data-ttu-id="44e8a-102">Operação ApplyIfC</span><span class="sxs-lookup"><span data-stu-id="44e8a-102">ApplyIfC operation</span></span>

<span data-ttu-id="44e8a-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="44e8a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="44e8a-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="44e8a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="44e8a-105">Aplica uma operação controlável condicionalmente em um bit clássico.</span><span class="sxs-lookup"><span data-stu-id="44e8a-105">Applies a controllable operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIfC<'T> (op : ('T => Unit is Ctl), bit : Bool, target : 'T) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="44e8a-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="44e8a-106">Description</span></span>

<span data-ttu-id="44e8a-107">Dada uma operação `op` e um valor de bit `bit` , aplica- `op` `target` se ao If `bit` is `true` .</span><span class="sxs-lookup"><span data-stu-id="44e8a-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="44e8a-108">Se `false` nada acontecer com o `target` .</span><span class="sxs-lookup"><span data-stu-id="44e8a-108">If `false`, nothing happens to the `target`.</span></span>
<span data-ttu-id="44e8a-109">O sufixo `C` indica que a operação a ser aplicada é controlável.</span><span class="sxs-lookup"><span data-stu-id="44e8a-109">The suffix `C` indicates that the operation to be applied is controllable.</span></span>

## <a name="input"></a><span data-ttu-id="44e8a-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="44e8a-110">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="44e8a-111">op: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é CTL</span><span class="sxs-lookup"><span data-stu-id="44e8a-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="44e8a-112">Uma operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="44e8a-112">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="44e8a-113">bit: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="44e8a-113">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="44e8a-114">um booliano que controla se op é aplicado ou não.</span><span class="sxs-lookup"><span data-stu-id="44e8a-114">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="44e8a-115">destino: ' t</span><span class="sxs-lookup"><span data-stu-id="44e8a-115">target : 'T</span></span>

<span data-ttu-id="44e8a-116">A entrada à qual a operação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="44e8a-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="44e8a-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="44e8a-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="44e8a-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="44e8a-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="44e8a-119">T'</span><span class="sxs-lookup"><span data-stu-id="44e8a-119">'T</span></span>

<span data-ttu-id="44e8a-120">O tipo de entrada da operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="44e8a-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="44e8a-121">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="44e8a-121">See Also</span></span>

- [<span data-ttu-id="44e8a-122">Microsoft. Quantum. Canon. ApplyIfC</span><span class="sxs-lookup"><span data-stu-id="44e8a-122">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="44e8a-123">Microsoft. Quantum. Canon. ApplyIfA</span><span class="sxs-lookup"><span data-stu-id="44e8a-123">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="44e8a-124">Microsoft. Quantum. Canon. ApplyIfCA</span><span class="sxs-lookup"><span data-stu-id="44e8a-124">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)