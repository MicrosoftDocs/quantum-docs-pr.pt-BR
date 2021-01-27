---
uid: Microsoft.Quantum.Canon.ApplyToHeadCA
title: Operação ApplyToHeadCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHeadCA
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 1bb24006a2d52167dfc7a7871cfbf5a4378d1cb7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850607"
---
# <a name="applytoheadca-operation"></a><span data-ttu-id="ffd77-102">Operação ApplyToHeadCA</span><span class="sxs-lookup"><span data-stu-id="ffd77-102">ApplyToHeadCA operation</span></span>

<span data-ttu-id="ffd77-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ffd77-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ffd77-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ffd77-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ffd77-105">Aplica uma operação ao primeiro elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="ffd77-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHeadCA<'T> (op : ('T => Unit is Adj + Ctl), targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="ffd77-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="ffd77-106">Description</span></span>

<span data-ttu-id="ffd77-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="ffd77-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="ffd77-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="ffd77-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="ffd77-109">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="ffd77-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="ffd77-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="ffd77-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="ffd77-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="ffd77-111">targets : 'T[]</span></span>

<span data-ttu-id="ffd77-112">Uma matriz de destinos, da qual a primeira será aplicada `op` .</span><span class="sxs-lookup"><span data-stu-id="ffd77-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ffd77-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ffd77-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ffd77-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="ffd77-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ffd77-115">T'</span><span class="sxs-lookup"><span data-stu-id="ffd77-115">'T</span></span>

<span data-ttu-id="ffd77-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="ffd77-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="ffd77-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ffd77-117">See Also</span></span>

- [<span data-ttu-id="ffd77-118">Microsoft. Quantum. Canon. ApplyToHead</span><span class="sxs-lookup"><span data-stu-id="ffd77-118">Microsoft.Quantum.Canon.ApplyToHead</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHead)
- [<span data-ttu-id="ffd77-119">Microsoft. Quantum. Canon. ApplyToHeadA</span><span class="sxs-lookup"><span data-stu-id="ffd77-119">Microsoft.Quantum.Canon.ApplyToHeadA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [<span data-ttu-id="ffd77-120">Microsoft. Quantum. Canon. ApplyToHeadC</span><span class="sxs-lookup"><span data-stu-id="ffd77-120">Microsoft.Quantum.Canon.ApplyToHeadC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadC)