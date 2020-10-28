---
uid: Microsoft.Quantum.Canon.ApplyToElement
title: Operação ApplyToElement
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElement
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: 5c321d95c9b79bc50827c2b50c406b164e143dc6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694199"
---
# <a name="applytoelement-operation"></a><span data-ttu-id="493f2-102">Operação ApplyToElement</span><span class="sxs-lookup"><span data-stu-id="493f2-102">ApplyToElement operation</span></span>

<span data-ttu-id="493f2-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="493f2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="493f2-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="493f2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="493f2-105">Aplica uma operação a um determinado elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="493f2-105">Applies an operation to a given element of an array.</span></span>

```qsharp
operation ApplyToElement<'T> (op : ('T => Unit), index : Int, targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="493f2-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="493f2-106">Description</span></span>

<span data-ttu-id="493f2-107">Dada uma operação `op` , um índice `index` e uma matriz de destinos `targets` , aplicam-se `op(targets[index])` .</span><span class="sxs-lookup"><span data-stu-id="493f2-107">Given an operation `op`, an index `index`, and an array of targets `targets`, applies `op(targets[index])`.</span></span>

## <a name="input"></a><span data-ttu-id="493f2-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="493f2-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="493f2-109">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="493f2-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="493f2-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="493f2-110">An operation to be applied.</span></span>


### <a name="index--int"></a><span data-ttu-id="493f2-111">índice: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="493f2-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="493f2-112">Um índice na matriz de destinos.</span><span class="sxs-lookup"><span data-stu-id="493f2-112">An index into the array of targets.</span></span>


### <a name="targets--t"></a><span data-ttu-id="493f2-113">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="493f2-113">targets : 'T[]</span></span>

<span data-ttu-id="493f2-114">Uma matriz de possíveis destinos para `op` .</span><span class="sxs-lookup"><span data-stu-id="493f2-114">An array of possible targets for `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="493f2-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="493f2-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="493f2-116">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="493f2-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="493f2-117">T'</span><span class="sxs-lookup"><span data-stu-id="493f2-117">'T</span></span>

<span data-ttu-id="493f2-118">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="493f2-118">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="493f2-119">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="493f2-119">See Also</span></span>

- [<span data-ttu-id="493f2-120">Microsoft. Quantum. Canon. ApplyToElementC</span><span class="sxs-lookup"><span data-stu-id="493f2-120">Microsoft.Quantum.Canon.ApplyToElementC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementC)
- [<span data-ttu-id="493f2-121">Microsoft. Quantum. Canon. ApplyToElementA</span><span class="sxs-lookup"><span data-stu-id="493f2-121">Microsoft.Quantum.Canon.ApplyToElementA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementA)
- [<span data-ttu-id="493f2-122">Microsoft. Quantum. Canon. ApplyToElementCA</span><span class="sxs-lookup"><span data-stu-id="493f2-122">Microsoft.Quantum.Canon.ApplyToElementCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementCA)