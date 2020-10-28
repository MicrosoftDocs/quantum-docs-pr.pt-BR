---
uid: Microsoft.Quantum.Canon.ApplyToHeadC
title: Operação ApplyToHeadC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHeadC
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 3ff6c25837f1219dd456bf1739a2953ff72e2df9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694162"
---
# <a name="applytoheadc-operation"></a><span data-ttu-id="738fb-102">Operação ApplyToHeadC</span><span class="sxs-lookup"><span data-stu-id="738fb-102">ApplyToHeadC operation</span></span>

<span data-ttu-id="738fb-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="738fb-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="738fb-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="738fb-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="738fb-105">Aplica uma operação ao primeiro elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="738fb-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHeadC<'T> (op : ('T => Unit is Ctl), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="738fb-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="738fb-106">Description</span></span>

<span data-ttu-id="738fb-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="738fb-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="738fb-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="738fb-108">Input</span></span>

### <a name="op--t--unit-ctl"></a><span data-ttu-id="738fb-109">op: ' t => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="738fb-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="738fb-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="738fb-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="738fb-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="738fb-111">targets : 'T[]</span></span>

<span data-ttu-id="738fb-112">Uma matriz de destinos, da qual a primeira será aplicada `op` .</span><span class="sxs-lookup"><span data-stu-id="738fb-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="738fb-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="738fb-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="738fb-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="738fb-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="738fb-115">T'</span><span class="sxs-lookup"><span data-stu-id="738fb-115">'T</span></span>

<span data-ttu-id="738fb-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="738fb-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="738fb-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="738fb-117">See Also</span></span>

- [<span data-ttu-id="738fb-118">Microsoft. Quantum. Canon. ApplyToHead</span><span class="sxs-lookup"><span data-stu-id="738fb-118">Microsoft.Quantum.Canon.ApplyToHead</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHead)
- [<span data-ttu-id="738fb-119">Microsoft. Quantum. Canon. ApplyToHeadA</span><span class="sxs-lookup"><span data-stu-id="738fb-119">Microsoft.Quantum.Canon.ApplyToHeadA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [<span data-ttu-id="738fb-120">Microsoft. Quantum. Canon. ApplyToHeadCA</span><span class="sxs-lookup"><span data-stu-id="738fb-120">Microsoft.Quantum.Canon.ApplyToHeadCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)