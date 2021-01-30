---
uid: Microsoft.Quantum.Canon.ApplyToElementCA
title: Operação ApplyToElementCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElementCA
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: 420a92ae10d2fc260024968b1846e669c4b62d73
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841464"
---
# <a name="applytoelementca-operation"></a><span data-ttu-id="a6691-102">Operação ApplyToElementCA</span><span class="sxs-lookup"><span data-stu-id="a6691-102">ApplyToElementCA operation</span></span>

<span data-ttu-id="a6691-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a6691-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a6691-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a6691-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a6691-105">Aplica uma operação a um determinado elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="a6691-105">Applies an operation to a given element of an array.</span></span>

```qsharp
operation ApplyToElementCA<'T> (op : ('T => Unit is Adj + Ctl), index : Int, targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="a6691-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="a6691-106">Description</span></span>

<span data-ttu-id="a6691-107">Dada uma operação `op` , um índice `index` e uma matriz de destinos `targets` , aplicam-se `op(targets[index])` .</span><span class="sxs-lookup"><span data-stu-id="a6691-107">Given an operation `op`, an index `index`, and an array of targets `targets`, applies `op(targets[index])`.</span></span>

## <a name="input"></a><span data-ttu-id="a6691-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="a6691-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="a6691-109">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="a6691-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="a6691-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="a6691-110">An operation to be applied.</span></span>


### <a name="index--int"></a><span data-ttu-id="a6691-111">índice: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a6691-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a6691-112">Um índice na matriz de destinos.</span><span class="sxs-lookup"><span data-stu-id="a6691-112">An index into the array of targets.</span></span>


### <a name="targets--t"></a><span data-ttu-id="a6691-113">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="a6691-113">targets : 'T[]</span></span>

<span data-ttu-id="a6691-114">Uma matriz de possíveis destinos para `op` .</span><span class="sxs-lookup"><span data-stu-id="a6691-114">An array of possible targets for `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a6691-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a6691-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a6691-116">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="a6691-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a6691-117">T'</span><span class="sxs-lookup"><span data-stu-id="a6691-117">'T</span></span>

<span data-ttu-id="a6691-118">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="a6691-118">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="a6691-119">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="a6691-119">See Also</span></span>

- [<span data-ttu-id="a6691-120">Microsoft. Quantum. Canon. ApplyToElement</span><span class="sxs-lookup"><span data-stu-id="a6691-120">Microsoft.Quantum.Canon.ApplyToElement</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElement)
- [<span data-ttu-id="a6691-121">Microsoft. Quantum. Canon. ApplyToElementC</span><span class="sxs-lookup"><span data-stu-id="a6691-121">Microsoft.Quantum.Canon.ApplyToElementC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementC)
- [<span data-ttu-id="a6691-122">Microsoft. Quantum. Canon. ApplyToElementA</span><span class="sxs-lookup"><span data-stu-id="a6691-122">Microsoft.Quantum.Canon.ApplyToElementA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementA)