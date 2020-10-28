---
uid: Microsoft.Quantum.Canon.ApplyIfOne
title: Operação ApplyIfOne
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOne
qsharp.summary: Applies an operation conditioned on a classical result value being one.
ms.openlocfilehash: 8c668423d126f02736bcb541e73e210a761c5719
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694284"
---
# <a name="applyifone-operation"></a><span data-ttu-id="ceb64-102">Operação ApplyIfOne</span><span class="sxs-lookup"><span data-stu-id="ceb64-102">ApplyIfOne operation</span></span>

<span data-ttu-id="ceb64-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ceb64-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ceb64-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ceb64-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ceb64-105">Aplica uma operação com condição em um valor de resultado clássico sendo um.</span><span class="sxs-lookup"><span data-stu-id="ceb64-105">Applies an operation conditioned on a classical result value being one.</span></span>

```qsharp
operation ApplyIfOne<'T> (result : Result, (op : ('T => Unit), target : 'T)) : Unit
```


## <a name="description"></a><span data-ttu-id="ceb64-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="ceb64-106">Description</span></span>

<span data-ttu-id="ceb64-107">Dada uma operação `op` e um valor de resultado `result` , aplica- `op` `target` se ao If `result` is `One` .</span><span class="sxs-lookup"><span data-stu-id="ceb64-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `One`.</span></span> <span data-ttu-id="ceb64-108">Se `Zero` nada acontecer com o `target` .</span><span class="sxs-lookup"><span data-stu-id="ceb64-108">If `Zero`, nothing happens to the `target`.</span></span>

## <a name="input"></a><span data-ttu-id="ceb64-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="ceb64-109">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="ceb64-110">resultado: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="ceb64-110">result : __invalid<Result>__</span></span>

<span data-ttu-id="ceb64-111">Um resultado de medida que controla se op é aplicado ou não.</span><span class="sxs-lookup"><span data-stu-id="ceb64-111">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit"></a><span data-ttu-id="ceb64-112">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="ceb64-112">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="ceb64-113">Uma operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="ceb64-113">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="ceb64-114">destino: ' t</span><span class="sxs-lookup"><span data-stu-id="ceb64-114">target : 'T</span></span>

<span data-ttu-id="ceb64-115">A entrada à qual a operação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="ceb64-115">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ceb64-116">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ceb64-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ceb64-117">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="ceb64-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ceb64-118">T'</span><span class="sxs-lookup"><span data-stu-id="ceb64-118">'T</span></span>

<span data-ttu-id="ceb64-119">O tipo de entrada da operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="ceb64-119">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="ceb64-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ceb64-120">See Also</span></span>

- [<span data-ttu-id="ceb64-121">Microsoft. Quantum. Canon. ApplyIfOneC</span><span class="sxs-lookup"><span data-stu-id="ceb64-121">Microsoft.Quantum.Canon.ApplyIfOneC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneC)
- [<span data-ttu-id="ceb64-122">Microsoft. Quantum. Canon. ApplyIfOneA</span><span class="sxs-lookup"><span data-stu-id="ceb64-122">Microsoft.Quantum.Canon.ApplyIfOneA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneA)
- [<span data-ttu-id="ceb64-123">Microsoft. Quantum. Canon. ApplyIfOneCA</span><span class="sxs-lookup"><span data-stu-id="ceb64-123">Microsoft.Quantum.Canon.ApplyIfOneCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneCA)