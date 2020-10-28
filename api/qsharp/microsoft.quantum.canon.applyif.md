---
uid: Microsoft.Quantum.Canon.ApplyIf
title: Operação ApplyIf
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIf
qsharp.summary: Applies an operation conditioned on a classical bit.
ms.openlocfilehash: c8f6860a7a3b8af86b0edb048baccbf057dd245a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694305"
---
# <a name="applyif-operation"></a><span data-ttu-id="58aeb-102">Operação ApplyIf</span><span class="sxs-lookup"><span data-stu-id="58aeb-102">ApplyIf operation</span></span>

<span data-ttu-id="58aeb-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="58aeb-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="58aeb-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="58aeb-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="58aeb-105">Aplica uma operação com condição em um bit clássico.</span><span class="sxs-lookup"><span data-stu-id="58aeb-105">Applies an operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIf<'T> (op : ('T => Unit), bit : Bool, target : 'T) : Unit
```


## <a name="description"></a><span data-ttu-id="58aeb-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="58aeb-106">Description</span></span>

<span data-ttu-id="58aeb-107">Dada uma operação `op` e um valor de bit `bit` , aplica- `op` `target` se ao If `bit` is `true` .</span><span class="sxs-lookup"><span data-stu-id="58aeb-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="58aeb-108">Se `false` nada acontecer com o `target` .</span><span class="sxs-lookup"><span data-stu-id="58aeb-108">If `false`, nothing happens to the `target`.</span></span>

## <a name="input"></a><span data-ttu-id="58aeb-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="58aeb-109">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="58aeb-110">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="58aeb-110">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="58aeb-111">Uma operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="58aeb-111">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="58aeb-112">bit: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="58aeb-112">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="58aeb-113">um booliano que controla se op é aplicado ou não.</span><span class="sxs-lookup"><span data-stu-id="58aeb-113">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="58aeb-114">destino: ' t</span><span class="sxs-lookup"><span data-stu-id="58aeb-114">target : 'T</span></span>

<span data-ttu-id="58aeb-115">A entrada à qual a operação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="58aeb-115">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="58aeb-116">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="58aeb-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="58aeb-117">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="58aeb-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="58aeb-118">T'</span><span class="sxs-lookup"><span data-stu-id="58aeb-118">'T</span></span>

<span data-ttu-id="58aeb-119">O tipo de entrada da operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="58aeb-119">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="58aeb-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="58aeb-120">See Also</span></span>

- [<span data-ttu-id="58aeb-121">Microsoft. Quantum. Canon. ApplyIfC</span><span class="sxs-lookup"><span data-stu-id="58aeb-121">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="58aeb-122">Microsoft. Quantum. Canon. ApplyIfA</span><span class="sxs-lookup"><span data-stu-id="58aeb-122">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="58aeb-123">Microsoft. Quantum. Canon. ApplyIfCA</span><span class="sxs-lookup"><span data-stu-id="58aeb-123">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)