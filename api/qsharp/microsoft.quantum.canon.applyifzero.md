---
uid: Microsoft.Quantum.Canon.ApplyIfZero
title: Operação ApplyIfZero
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfZero
qsharp.summary: Applies an operation conditioned on a classical result value being zero.
ms.openlocfilehash: 7435150937143a8d1a67afe334b683932a9655de
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694278"
---
# <a name="applyifzero-operation"></a><span data-ttu-id="9758f-102">Operação ApplyIfZero</span><span class="sxs-lookup"><span data-stu-id="9758f-102">ApplyIfZero operation</span></span>

<span data-ttu-id="9758f-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9758f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9758f-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9758f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9758f-105">Aplica uma operação com condição em um valor de resultado clássico igual a zero.</span><span class="sxs-lookup"><span data-stu-id="9758f-105">Applies an operation conditioned on a classical result value being zero.</span></span>

```qsharp
operation ApplyIfZero<'T> (result : Result, (op : ('T => Unit), target : 'T)) : Unit
```


## <a name="description"></a><span data-ttu-id="9758f-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="9758f-106">Description</span></span>

<span data-ttu-id="9758f-107">Dada uma operação `op` e um valor de resultado `result` , aplica- `op` `target` se ao If `result` is `Zero` .</span><span class="sxs-lookup"><span data-stu-id="9758f-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `Zero`.</span></span> <span data-ttu-id="9758f-108">Se `One` nada acontecer com o `target` .</span><span class="sxs-lookup"><span data-stu-id="9758f-108">If `One`, nothing happens to the `target`.</span></span>

## <a name="input"></a><span data-ttu-id="9758f-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="9758f-109">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="9758f-110">resultado: __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="9758f-110">result : __invalid<Result>__</span></span>

<span data-ttu-id="9758f-111">Um resultado de medida que controla se op é aplicado ou não.</span><span class="sxs-lookup"><span data-stu-id="9758f-111">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit"></a><span data-ttu-id="9758f-112">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="9758f-112">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="9758f-113">Uma operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="9758f-113">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="9758f-114">destino: ' t</span><span class="sxs-lookup"><span data-stu-id="9758f-114">target : 'T</span></span>

<span data-ttu-id="9758f-115">A entrada à qual a operação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="9758f-115">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9758f-116">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9758f-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="9758f-117">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="9758f-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9758f-118">T'</span><span class="sxs-lookup"><span data-stu-id="9758f-118">'T</span></span>

<span data-ttu-id="9758f-119">O tipo de entrada da operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="9758f-119">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="9758f-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="9758f-120">See Also</span></span>

- [<span data-ttu-id="9758f-121">Microsoft. Quantum. Canon. ApplyIfZeroC</span><span class="sxs-lookup"><span data-stu-id="9758f-121">Microsoft.Quantum.Canon.ApplyIfZeroC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroC)
- [<span data-ttu-id="9758f-122">Microsoft. Quantum. Canon. ApplyIfZeroA</span><span class="sxs-lookup"><span data-stu-id="9758f-122">Microsoft.Quantum.Canon.ApplyIfZeroA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroA)
- [<span data-ttu-id="9758f-123">Microsoft. Quantum. Canon. ApplyIfZeroCA</span><span class="sxs-lookup"><span data-stu-id="9758f-123">Microsoft.Quantum.Canon.ApplyIfZeroCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroCA)