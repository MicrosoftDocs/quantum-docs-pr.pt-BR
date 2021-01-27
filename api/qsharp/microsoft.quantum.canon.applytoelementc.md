---
uid: Microsoft.Quantum.Canon.ApplyToElementC
title: Operação ApplyToElementC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElementC
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: bc63b6b591781a6283b872ef0c2509094a656b4c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850755"
---
# <a name="applytoelementc-operation"></a><span data-ttu-id="b7b39-102">Operação ApplyToElementC</span><span class="sxs-lookup"><span data-stu-id="b7b39-102">ApplyToElementC operation</span></span>

<span data-ttu-id="b7b39-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b7b39-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b7b39-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b7b39-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b7b39-105">Aplica uma operação a um determinado elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="b7b39-105">Applies an operation to a given element of an array.</span></span>

```qsharp
operation ApplyToElementC<'T> (op : ('T => Unit is Ctl), index : Int, targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="b7b39-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7b39-106">Description</span></span>

<span data-ttu-id="b7b39-107">Dada uma operação `op` , um índice `index` e uma matriz de destinos `targets` , aplicam-se `op(targets[index])` .</span><span class="sxs-lookup"><span data-stu-id="b7b39-107">Given an operation `op`, an index `index`, and an array of targets `targets`, applies `op(targets[index])`.</span></span>

## <a name="input"></a><span data-ttu-id="b7b39-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="b7b39-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="b7b39-109">op: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é CTL</span><span class="sxs-lookup"><span data-stu-id="b7b39-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="b7b39-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="b7b39-110">An operation to be applied.</span></span>


### <a name="index--int"></a><span data-ttu-id="b7b39-111">índice: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b7b39-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b7b39-112">Um índice na matriz de destinos.</span><span class="sxs-lookup"><span data-stu-id="b7b39-112">An index into the array of targets.</span></span>


### <a name="targets--t"></a><span data-ttu-id="b7b39-113">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="b7b39-113">targets : 'T[]</span></span>

<span data-ttu-id="b7b39-114">Uma matriz de possíveis destinos para `op` .</span><span class="sxs-lookup"><span data-stu-id="b7b39-114">An array of possible targets for `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b7b39-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b7b39-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="b7b39-116">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="b7b39-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b7b39-117">T'</span><span class="sxs-lookup"><span data-stu-id="b7b39-117">'T</span></span>

<span data-ttu-id="b7b39-118">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="b7b39-118">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="b7b39-119">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="b7b39-119">See Also</span></span>

- [<span data-ttu-id="b7b39-120">Microsoft. Quantum. Canon. ApplyToElement</span><span class="sxs-lookup"><span data-stu-id="b7b39-120">Microsoft.Quantum.Canon.ApplyToElement</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElement)
- [<span data-ttu-id="b7b39-121">Microsoft. Quantum. Canon. ApplyToElementA</span><span class="sxs-lookup"><span data-stu-id="b7b39-121">Microsoft.Quantum.Canon.ApplyToElementA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementA)
- [<span data-ttu-id="b7b39-122">Microsoft. Quantum. Canon. ApplyToElementCA</span><span class="sxs-lookup"><span data-stu-id="b7b39-122">Microsoft.Quantum.Canon.ApplyToElementCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementCA)