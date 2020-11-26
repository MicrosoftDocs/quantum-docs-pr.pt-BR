---
uid: Microsoft.Quantum.Canon.ApplyIfOneCA
title: Operação ApplyIfOneCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOneCA
qsharp.summary: Applies a unitary operation conditioned on a classical result value being one.
ms.openlocfilehash: 29801ed0bec08d0ab818f237feb17c2a2a7af1e4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218573"
---
# <a name="applyifoneca-operation"></a><span data-ttu-id="eb4fc-102">Operação ApplyIfOneCA</span><span class="sxs-lookup"><span data-stu-id="eb4fc-102">ApplyIfOneCA operation</span></span>

<span data-ttu-id="eb4fc-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="eb4fc-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="eb4fc-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="eb4fc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="eb4fc-105">Aplica uma operação unitário com condição em um valor de resultado clássico sendo um.</span><span class="sxs-lookup"><span data-stu-id="eb4fc-105">Applies a unitary operation conditioned on a classical result value being one.</span></span>

```qsharp
operation ApplyIfOneCA<'T> (result : Result, (op : ('T => Unit is Adj + Ctl), target : 'T)) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="eb4fc-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="eb4fc-106">Description</span></span>

<span data-ttu-id="eb4fc-107">Dada uma operação `op` e um valor de resultado `result` , aplica- `op` `target` se ao If `result` is `One` .</span><span class="sxs-lookup"><span data-stu-id="eb4fc-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `One`.</span></span> <span data-ttu-id="eb4fc-108">Se `Zero` nada acontecer com o `target` .</span><span class="sxs-lookup"><span data-stu-id="eb4fc-108">If `Zero`, nothing happens to the `target`.</span></span>
<span data-ttu-id="eb4fc-109">O sufixo `CA` indica que a operação a ser aplicada é unitário (controlável e adjacenttable).</span><span class="sxs-lookup"><span data-stu-id="eb4fc-109">The suffix `CA` indicates that the operation to be applied is unitary (controllable and adjointable).</span></span>

## <a name="input"></a><span data-ttu-id="eb4fc-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="eb4fc-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="eb4fc-111">resultado: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="eb4fc-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="eb4fc-112">Um resultado de medida que controla se op é aplicado ou não.</span><span class="sxs-lookup"><span data-stu-id="eb4fc-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="eb4fc-113">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="eb4fc-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="eb4fc-114">Uma operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="eb4fc-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="eb4fc-115">destino: ' t</span><span class="sxs-lookup"><span data-stu-id="eb4fc-115">target : 'T</span></span>

<span data-ttu-id="eb4fc-116">A entrada à qual a operação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="eb4fc-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="eb4fc-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="eb4fc-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="eb4fc-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="eb4fc-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="eb4fc-119">T'</span><span class="sxs-lookup"><span data-stu-id="eb4fc-119">'T</span></span>

<span data-ttu-id="eb4fc-120">O tipo de entrada da operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="eb4fc-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="eb4fc-121">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="eb4fc-121">See Also</span></span>

- [<span data-ttu-id="eb4fc-122">Microsoft. Quantum. Canon. ApplyIfOneC</span><span class="sxs-lookup"><span data-stu-id="eb4fc-122">Microsoft.Quantum.Canon.ApplyIfOneC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneC)
- [<span data-ttu-id="eb4fc-123">Microsoft. Quantum. Canon. ApplyIfOneA</span><span class="sxs-lookup"><span data-stu-id="eb4fc-123">Microsoft.Quantum.Canon.ApplyIfOneA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneA)
- [<span data-ttu-id="eb4fc-124">Microsoft. Quantum. Canon. ApplyIfOneCA</span><span class="sxs-lookup"><span data-stu-id="eb4fc-124">Microsoft.Quantum.Canon.ApplyIfOneCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneCA)