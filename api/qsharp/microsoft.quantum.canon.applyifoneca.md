---
uid: Microsoft.Quantum.Canon.ApplyIfOneCA
title: Operação ApplyIfOneCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOneCA
qsharp.summary: Applies a unitary operation conditioned on a classical result value being one.
ms.openlocfilehash: 8b27a192c66a127fe5a8acfbba7b78314988bf2e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844924"
---
# <a name="applyifoneca-operation"></a><span data-ttu-id="b0614-102">Operação ApplyIfOneCA</span><span class="sxs-lookup"><span data-stu-id="b0614-102">ApplyIfOneCA operation</span></span>

<span data-ttu-id="b0614-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b0614-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b0614-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b0614-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b0614-105">Aplica uma operação unitário com condição em um valor de resultado clássico sendo um.</span><span class="sxs-lookup"><span data-stu-id="b0614-105">Applies a unitary operation conditioned on a classical result value being one.</span></span>

```qsharp
operation ApplyIfOneCA<'T> (result : Result, (op : ('T => Unit is Adj + Ctl), target : 'T)) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="b0614-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0614-106">Description</span></span>

<span data-ttu-id="b0614-107">Dada uma operação `op` e um valor de resultado `result` , aplica- `op` `target` se ao If `result` is `One` .</span><span class="sxs-lookup"><span data-stu-id="b0614-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `One`.</span></span> <span data-ttu-id="b0614-108">Se `Zero` nada acontecer com o `target` .</span><span class="sxs-lookup"><span data-stu-id="b0614-108">If `Zero`, nothing happens to the `target`.</span></span>
<span data-ttu-id="b0614-109">O sufixo `CA` indica que a operação a ser aplicada é unitário (controlável e adjacenttable).</span><span class="sxs-lookup"><span data-stu-id="b0614-109">The suffix `CA` indicates that the operation to be applied is unitary (controllable and adjointable).</span></span>

## <a name="input"></a><span data-ttu-id="b0614-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="b0614-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="b0614-111">resultado: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="b0614-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="b0614-112">Um resultado de medida que controla se op é aplicado ou não.</span><span class="sxs-lookup"><span data-stu-id="b0614-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="b0614-113">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="b0614-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="b0614-114">Uma operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="b0614-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="b0614-115">destino: ' t</span><span class="sxs-lookup"><span data-stu-id="b0614-115">target : 'T</span></span>

<span data-ttu-id="b0614-116">A entrada à qual a operação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="b0614-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b0614-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b0614-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="b0614-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="b0614-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b0614-119">T'</span><span class="sxs-lookup"><span data-stu-id="b0614-119">'T</span></span>

<span data-ttu-id="b0614-120">O tipo de entrada da operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="b0614-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="b0614-121">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="b0614-121">See Also</span></span>

- [<span data-ttu-id="b0614-122">Microsoft. Quantum. Canon. ApplyIfOneC</span><span class="sxs-lookup"><span data-stu-id="b0614-122">Microsoft.Quantum.Canon.ApplyIfOneC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneC)
- [<span data-ttu-id="b0614-123">Microsoft. Quantum. Canon. ApplyIfOneA</span><span class="sxs-lookup"><span data-stu-id="b0614-123">Microsoft.Quantum.Canon.ApplyIfOneA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneA)
- [<span data-ttu-id="b0614-124">Microsoft. Quantum. Canon. ApplyIfOneCA</span><span class="sxs-lookup"><span data-stu-id="b0614-124">Microsoft.Quantum.Canon.ApplyIfOneCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneCA)