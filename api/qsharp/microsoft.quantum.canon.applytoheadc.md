---
uid: Microsoft.Quantum.Canon.ApplyToHeadC
title: Operação ApplyToHeadC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHeadC
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 3a65ad52e0b2f8b3a921fc549c35311f24d0e189
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850620"
---
# <a name="applytoheadc-operation"></a><span data-ttu-id="fb9b7-102">Operação ApplyToHeadC</span><span class="sxs-lookup"><span data-stu-id="fb9b7-102">ApplyToHeadC operation</span></span>

<span data-ttu-id="fb9b7-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="fb9b7-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="fb9b7-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fb9b7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fb9b7-105">Aplica uma operação ao primeiro elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="fb9b7-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHeadC<'T> (op : ('T => Unit is Ctl), targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="fb9b7-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb9b7-106">Description</span></span>

<span data-ttu-id="fb9b7-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="fb9b7-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="fb9b7-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="fb9b7-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="fb9b7-109">op: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é CTL</span><span class="sxs-lookup"><span data-stu-id="fb9b7-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="fb9b7-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="fb9b7-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="fb9b7-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="fb9b7-111">targets : 'T[]</span></span>

<span data-ttu-id="fb9b7-112">Uma matriz de destinos, da qual a primeira será aplicada `op` .</span><span class="sxs-lookup"><span data-stu-id="fb9b7-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="fb9b7-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fb9b7-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="fb9b7-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="fb9b7-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="fb9b7-115">T'</span><span class="sxs-lookup"><span data-stu-id="fb9b7-115">'T</span></span>

<span data-ttu-id="fb9b7-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="fb9b7-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="fb9b7-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="fb9b7-117">See Also</span></span>

- [<span data-ttu-id="fb9b7-118">Microsoft. Quantum. Canon. ApplyToHead</span><span class="sxs-lookup"><span data-stu-id="fb9b7-118">Microsoft.Quantum.Canon.ApplyToHead</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHead)
- [<span data-ttu-id="fb9b7-119">Microsoft. Quantum. Canon. ApplyToHeadA</span><span class="sxs-lookup"><span data-stu-id="fb9b7-119">Microsoft.Quantum.Canon.ApplyToHeadA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [<span data-ttu-id="fb9b7-120">Microsoft. Quantum. Canon. ApplyToHeadCA</span><span class="sxs-lookup"><span data-stu-id="fb9b7-120">Microsoft.Quantum.Canon.ApplyToHeadCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)