---
uid: Microsoft.Quantum.Canon.ApplyIfZeroA
title: Operação ApplyIfZeroA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfZeroA
qsharp.summary: Applies an adjointable operation conditioned on a classical result value being zero.
ms.openlocfilehash: d324cd970e8df49ceb51b6bf5c9f3c9c3ff142f9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694277"
---
# <a name="applyifzeroa-operation"></a><span data-ttu-id="5286b-102">Operação ApplyIfZeroA</span><span class="sxs-lookup"><span data-stu-id="5286b-102">ApplyIfZeroA operation</span></span>

<span data-ttu-id="5286b-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5286b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5286b-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5286b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5286b-105">Aplica uma operação de modo adjacente condicional em um valor de resultado clássico como zero.</span><span class="sxs-lookup"><span data-stu-id="5286b-105">Applies an adjointable operation conditioned on a classical result value being zero.</span></span>

```qsharp
operation ApplyIfZeroA<'T> (result : Result, (op : ('T => Unit is Adj), target : 'T)) : Unit
```


## <a name="description"></a><span data-ttu-id="5286b-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="5286b-106">Description</span></span>

<span data-ttu-id="5286b-107">Dada uma operação `op` e um valor de resultado `result` , aplica- `op` `target` se ao If `result` is `Zero` .</span><span class="sxs-lookup"><span data-stu-id="5286b-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `Zero`.</span></span> <span data-ttu-id="5286b-108">Se `One` nada acontecer com o `target` .</span><span class="sxs-lookup"><span data-stu-id="5286b-108">If `One`, nothing happens to the `target`.</span></span>
<span data-ttu-id="5286b-109">O sufixo `A` indica que a operação a ser aplicada é adjointable.</span><span class="sxs-lookup"><span data-stu-id="5286b-109">The suffix `A` indicates that the operation to be applied is adjointable.</span></span>

## <a name="input"></a><span data-ttu-id="5286b-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="5286b-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="5286b-111">resultado: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="5286b-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="5286b-112">Um resultado de medida que controla se op é aplicado ou não.</span><span class="sxs-lookup"><span data-stu-id="5286b-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit-adj"></a><span data-ttu-id="5286b-113">op: ' t => adj de [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5286b-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="5286b-114">Uma operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="5286b-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="5286b-115">destino: ' t</span><span class="sxs-lookup"><span data-stu-id="5286b-115">target : 'T</span></span>

<span data-ttu-id="5286b-116">A entrada à qual a operação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="5286b-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5286b-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5286b-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="5286b-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="5286b-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5286b-119">T'</span><span class="sxs-lookup"><span data-stu-id="5286b-119">'T</span></span>

<span data-ttu-id="5286b-120">O tipo de entrada da operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="5286b-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="5286b-121">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="5286b-121">See Also</span></span>

- [<span data-ttu-id="5286b-122">Microsoft. Quantum. Canon. ApplyIfZeroC</span><span class="sxs-lookup"><span data-stu-id="5286b-122">Microsoft.Quantum.Canon.ApplyIfZeroC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroC)
- [<span data-ttu-id="5286b-123">Microsoft. Quantum. Canon. ApplyIfZeroA</span><span class="sxs-lookup"><span data-stu-id="5286b-123">Microsoft.Quantum.Canon.ApplyIfZeroA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroA)
- [<span data-ttu-id="5286b-124">Microsoft. Quantum. Canon. ApplyIfZeroCA</span><span class="sxs-lookup"><span data-stu-id="5286b-124">Microsoft.Quantum.Canon.ApplyIfZeroCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroCA)