---
uid: Microsoft.Quantum.Canon.ApplyIfZeroCA
title: Operação ApplyIfZeroCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfZeroCA
qsharp.summary: Applies a unitary operation conditioned on a classical result value being zero.
ms.openlocfilehash: 4ed0660e2fe3623d0a8e4e4f3bd0bddb536b7b5c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844888"
---
# <a name="applyifzeroca-operation"></a><span data-ttu-id="58846-102">Operação ApplyIfZeroCA</span><span class="sxs-lookup"><span data-stu-id="58846-102">ApplyIfZeroCA operation</span></span>

<span data-ttu-id="58846-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="58846-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="58846-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="58846-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="58846-105">Aplica uma operação unitário com condição em um valor de resultado clássico igual a zero.</span><span class="sxs-lookup"><span data-stu-id="58846-105">Applies a unitary operation conditioned on a classical result value being zero.</span></span>

```qsharp
operation ApplyIfZeroCA<'T> (result : Result, (op : ('T => Unit is Adj + Ctl), target : 'T)) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="58846-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="58846-106">Description</span></span>

<span data-ttu-id="58846-107">Dada uma operação `op` e um valor de resultado `result` , aplica- `op` `target` se ao If `result` is `Zero` .</span><span class="sxs-lookup"><span data-stu-id="58846-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `Zero`.</span></span> <span data-ttu-id="58846-108">Se `One` nada acontecer com o `target` .</span><span class="sxs-lookup"><span data-stu-id="58846-108">If `One`, nothing happens to the `target`.</span></span>
<span data-ttu-id="58846-109">O sufixo `CA` indica que a operação a ser aplicada é unitário (controlável e adjacenttable).</span><span class="sxs-lookup"><span data-stu-id="58846-109">The suffix `CA` indicates that the operation to be applied is unitary (controllable and adjointable).</span></span>

## <a name="input"></a><span data-ttu-id="58846-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="58846-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="58846-111">resultado: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="58846-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="58846-112">Um resultado de medida que controla se op é aplicado ou não.</span><span class="sxs-lookup"><span data-stu-id="58846-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="58846-113">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="58846-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="58846-114">Uma operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="58846-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="58846-115">destino: ' t</span><span class="sxs-lookup"><span data-stu-id="58846-115">target : 'T</span></span>

<span data-ttu-id="58846-116">A entrada à qual a operação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="58846-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="58846-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="58846-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="58846-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="58846-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="58846-119">T'</span><span class="sxs-lookup"><span data-stu-id="58846-119">'T</span></span>

<span data-ttu-id="58846-120">O tipo de entrada da operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="58846-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="58846-121">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="58846-121">See Also</span></span>

- [<span data-ttu-id="58846-122">Microsoft. Quantum. Canon. ApplyIfZeroC</span><span class="sxs-lookup"><span data-stu-id="58846-122">Microsoft.Quantum.Canon.ApplyIfZeroC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroC)
- [<span data-ttu-id="58846-123">Microsoft. Quantum. Canon. ApplyIfZeroA</span><span class="sxs-lookup"><span data-stu-id="58846-123">Microsoft.Quantum.Canon.ApplyIfZeroA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroA)
- [<span data-ttu-id="58846-124">Microsoft. Quantum. Canon. ApplyIfZeroCA</span><span class="sxs-lookup"><span data-stu-id="58846-124">Microsoft.Quantum.Canon.ApplyIfZeroCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroCA)