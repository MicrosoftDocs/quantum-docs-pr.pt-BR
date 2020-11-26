---
uid: Microsoft.Quantum.Canon.ApplyIfOneA
title: Operação ApplyIfOneA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOneA
qsharp.summary: Applies an adjointable operation conditioned on a classical result value being one.
ms.openlocfilehash: 200908f2958b74e4823c891ef901474d75d18336
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218539"
---
# <a name="applyifonea-operation"></a><span data-ttu-id="ae08f-102">Operação ApplyIfOneA</span><span class="sxs-lookup"><span data-stu-id="ae08f-102">ApplyIfOneA operation</span></span>

<span data-ttu-id="ae08f-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ae08f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ae08f-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ae08f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ae08f-105">Aplica uma operação de modo adjacente condição em um valor de resultado clássico sendo um.</span><span class="sxs-lookup"><span data-stu-id="ae08f-105">Applies an adjointable operation conditioned on a classical result value being one.</span></span>

```qsharp
operation ApplyIfOneA<'T> (result : Result, (op : ('T => Unit is Adj), target : 'T)) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="ae08f-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="ae08f-106">Description</span></span>

<span data-ttu-id="ae08f-107">Dada uma operação `op` e um valor de resultado `result` , aplica- `op` `target` se ao If `result` is `One` .</span><span class="sxs-lookup"><span data-stu-id="ae08f-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `One`.</span></span> <span data-ttu-id="ae08f-108">Se `Zero` nada acontecer com o `target` .</span><span class="sxs-lookup"><span data-stu-id="ae08f-108">If `Zero`, nothing happens to the `target`.</span></span>
<span data-ttu-id="ae08f-109">O sufixo `A` indica que a operação a ser aplicada é adjointable.</span><span class="sxs-lookup"><span data-stu-id="ae08f-109">The suffix `A` indicates that the operation to be applied is adjointable.</span></span>

## <a name="input"></a><span data-ttu-id="ae08f-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="ae08f-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="ae08f-111">resultado: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="ae08f-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="ae08f-112">Um resultado de medida que controla se op é aplicado ou não.</span><span class="sxs-lookup"><span data-stu-id="ae08f-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit--is-adj"></a><span data-ttu-id="ae08f-113">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="ae08f-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="ae08f-114">Uma operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="ae08f-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="ae08f-115">destino: ' t</span><span class="sxs-lookup"><span data-stu-id="ae08f-115">target : 'T</span></span>

<span data-ttu-id="ae08f-116">A entrada à qual a operação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="ae08f-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ae08f-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ae08f-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ae08f-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="ae08f-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ae08f-119">T'</span><span class="sxs-lookup"><span data-stu-id="ae08f-119">'T</span></span>

<span data-ttu-id="ae08f-120">O tipo de entrada da operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="ae08f-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="ae08f-121">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ae08f-121">See Also</span></span>

- [<span data-ttu-id="ae08f-122">Microsoft. Quantum. Canon. ApplyIfOneC</span><span class="sxs-lookup"><span data-stu-id="ae08f-122">Microsoft.Quantum.Canon.ApplyIfOneC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneC)
- [<span data-ttu-id="ae08f-123">Microsoft. Quantum. Canon. ApplyIfOneA</span><span class="sxs-lookup"><span data-stu-id="ae08f-123">Microsoft.Quantum.Canon.ApplyIfOneA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneA)
- [<span data-ttu-id="ae08f-124">Microsoft. Quantum. Canon. ApplyIfOneCA</span><span class="sxs-lookup"><span data-stu-id="ae08f-124">Microsoft.Quantum.Canon.ApplyIfOneCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneCA)