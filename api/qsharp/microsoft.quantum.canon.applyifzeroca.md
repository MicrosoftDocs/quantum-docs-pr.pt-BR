---
uid: Microsoft.Quantum.Canon.ApplyIfZeroCA
title: Operação ApplyIfZeroCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfZeroCA
qsharp.summary: Applies a unitary operation conditioned on a classical result value being zero.
ms.openlocfilehash: 85612bd3dd7af45b7901fef775a7d556eb229608
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694270"
---
# <a name="applyifzeroca-operation"></a><span data-ttu-id="b296e-102">Operação ApplyIfZeroCA</span><span class="sxs-lookup"><span data-stu-id="b296e-102">ApplyIfZeroCA operation</span></span>

<span data-ttu-id="b296e-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b296e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b296e-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b296e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b296e-105">Aplica uma operação unitário com condição em um valor de resultado clássico igual a zero.</span><span class="sxs-lookup"><span data-stu-id="b296e-105">Applies a unitary operation conditioned on a classical result value being zero.</span></span>

```qsharp
operation ApplyIfZeroCA<'T> (result : Result, (op : ('T => Unit is Adj + Ctl), target : 'T)) : Unit
```


## <a name="description"></a><span data-ttu-id="b296e-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="b296e-106">Description</span></span>

<span data-ttu-id="b296e-107">Dada uma operação `op` e um valor de resultado `result` , aplica- `op` `target` se ao If `result` is `Zero` .</span><span class="sxs-lookup"><span data-stu-id="b296e-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `Zero`.</span></span> <span data-ttu-id="b296e-108">Se `One` nada acontecer com o `target` .</span><span class="sxs-lookup"><span data-stu-id="b296e-108">If `One`, nothing happens to the `target`.</span></span>
<span data-ttu-id="b296e-109">O sufixo `CA` indica que a operação a ser aplicada é unitário (controlável e adjacenttable).</span><span class="sxs-lookup"><span data-stu-id="b296e-109">The suffix `CA` indicates that the operation to be applied is unitary (controllable and adjointable).</span></span>

## <a name="input"></a><span data-ttu-id="b296e-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="b296e-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="b296e-111">resultado: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="b296e-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="b296e-112">Um resultado de medida que controla se op é aplicado ou não.</span><span class="sxs-lookup"><span data-stu-id="b296e-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit-adj--ctl"></a><span data-ttu-id="b296e-113">op: ' t => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL</span><span class="sxs-lookup"><span data-stu-id="b296e-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="b296e-114">Uma operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="b296e-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="b296e-115">destino: ' t</span><span class="sxs-lookup"><span data-stu-id="b296e-115">target : 'T</span></span>

<span data-ttu-id="b296e-116">A entrada à qual a operação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="b296e-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b296e-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b296e-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="b296e-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="b296e-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b296e-119">T'</span><span class="sxs-lookup"><span data-stu-id="b296e-119">'T</span></span>

<span data-ttu-id="b296e-120">O tipo de entrada da operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="b296e-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="b296e-121">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="b296e-121">See Also</span></span>

- [<span data-ttu-id="b296e-122">Microsoft. Quantum. Canon. ApplyIfZeroC</span><span class="sxs-lookup"><span data-stu-id="b296e-122">Microsoft.Quantum.Canon.ApplyIfZeroC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroC)
- [<span data-ttu-id="b296e-123">Microsoft. Quantum. Canon. ApplyIfZeroA</span><span class="sxs-lookup"><span data-stu-id="b296e-123">Microsoft.Quantum.Canon.ApplyIfZeroA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroA)
- [<span data-ttu-id="b296e-124">Microsoft. Quantum. Canon. ApplyIfZeroCA</span><span class="sxs-lookup"><span data-stu-id="b296e-124">Microsoft.Quantum.Canon.ApplyIfZeroCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroCA)