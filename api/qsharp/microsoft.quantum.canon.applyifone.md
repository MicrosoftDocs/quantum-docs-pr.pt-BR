---
uid: Microsoft.Quantum.Canon.ApplyIfOne
title: Operação ApplyIfOne
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOne
qsharp.summary: Applies an operation conditioned on a classical result value being one.
ms.openlocfilehash: b7c07e01ebcaf2d475283bea0695aa68dd10776e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209393"
---
# <a name="applyifone-operation"></a><span data-ttu-id="37ccf-102">Operação ApplyIfOne</span><span class="sxs-lookup"><span data-stu-id="37ccf-102">ApplyIfOne operation</span></span>

<span data-ttu-id="37ccf-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="37ccf-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="37ccf-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="37ccf-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="37ccf-105">Aplica uma operação com condição em um valor de resultado clássico sendo um.</span><span class="sxs-lookup"><span data-stu-id="37ccf-105">Applies an operation conditioned on a classical result value being one.</span></span>

```qsharp
operation ApplyIfOne<'T> (result : Result, (op : ('T => Unit), target : 'T)) : Unit
```


## <a name="description"></a><span data-ttu-id="37ccf-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="37ccf-106">Description</span></span>

<span data-ttu-id="37ccf-107">Dada uma operação `op` e um valor de resultado `result` , aplica- `op` `target` se ao If `result` is `One` .</span><span class="sxs-lookup"><span data-stu-id="37ccf-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `One`.</span></span> <span data-ttu-id="37ccf-108">Se `Zero` nada acontecer com o `target` .</span><span class="sxs-lookup"><span data-stu-id="37ccf-108">If `Zero`, nothing happens to the `target`.</span></span>

## <a name="input"></a><span data-ttu-id="37ccf-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="37ccf-109">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="37ccf-110">resultado: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="37ccf-110">result : __invalid<Result>__</span></span>

<span data-ttu-id="37ccf-111">Um resultado de medida que controla se op é aplicado ou não.</span><span class="sxs-lookup"><span data-stu-id="37ccf-111">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit"></a><span data-ttu-id="37ccf-112">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="37ccf-112">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="37ccf-113">Uma operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="37ccf-113">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="37ccf-114">destino: ' t</span><span class="sxs-lookup"><span data-stu-id="37ccf-114">target : 'T</span></span>

<span data-ttu-id="37ccf-115">A entrada à qual a operação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="37ccf-115">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="37ccf-116">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="37ccf-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="37ccf-117">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="37ccf-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="37ccf-118">T'</span><span class="sxs-lookup"><span data-stu-id="37ccf-118">'T</span></span>

<span data-ttu-id="37ccf-119">O tipo de entrada da operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="37ccf-119">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="37ccf-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="37ccf-120">See Also</span></span>

- [<span data-ttu-id="37ccf-121">Microsoft. Quantum. Canon. ApplyIfOneC</span><span class="sxs-lookup"><span data-stu-id="37ccf-121">Microsoft.Quantum.Canon.ApplyIfOneC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneC)
- [<span data-ttu-id="37ccf-122">Microsoft. Quantum. Canon. ApplyIfOneA</span><span class="sxs-lookup"><span data-stu-id="37ccf-122">Microsoft.Quantum.Canon.ApplyIfOneA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneA)
- [<span data-ttu-id="37ccf-123">Microsoft. Quantum. Canon. ApplyIfOneCA</span><span class="sxs-lookup"><span data-stu-id="37ccf-123">Microsoft.Quantum.Canon.ApplyIfOneCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneCA)