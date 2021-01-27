---
uid: Microsoft.Quantum.Canon.ApplyToElement
title: Operação ApplyToElement
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElement
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: 5159eee07f7398cc6194c9907a37b78a63aaf263
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850789"
---
# <a name="applytoelement-operation"></a><span data-ttu-id="2ad6c-102">Operação ApplyToElement</span><span class="sxs-lookup"><span data-stu-id="2ad6c-102">ApplyToElement operation</span></span>

<span data-ttu-id="2ad6c-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="2ad6c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="2ad6c-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2ad6c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2ad6c-105">Aplica uma operação a um determinado elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="2ad6c-105">Applies an operation to a given element of an array.</span></span>

```qsharp
operation ApplyToElement<'T> (op : ('T => Unit), index : Int, targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="2ad6c-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="2ad6c-106">Description</span></span>

<span data-ttu-id="2ad6c-107">Dada uma operação `op` , um índice `index` e uma matriz de destinos `targets` , aplicam-se `op(targets[index])` .</span><span class="sxs-lookup"><span data-stu-id="2ad6c-107">Given an operation `op`, an index `index`, and an array of targets `targets`, applies `op(targets[index])`.</span></span>

## <a name="input"></a><span data-ttu-id="2ad6c-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="2ad6c-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="2ad6c-109">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="2ad6c-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="2ad6c-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="2ad6c-110">An operation to be applied.</span></span>


### <a name="index--int"></a><span data-ttu-id="2ad6c-111">índice: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2ad6c-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2ad6c-112">Um índice na matriz de destinos.</span><span class="sxs-lookup"><span data-stu-id="2ad6c-112">An index into the array of targets.</span></span>


### <a name="targets--t"></a><span data-ttu-id="2ad6c-113">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="2ad6c-113">targets : 'T[]</span></span>

<span data-ttu-id="2ad6c-114">Uma matriz de possíveis destinos para `op` .</span><span class="sxs-lookup"><span data-stu-id="2ad6c-114">An array of possible targets for `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2ad6c-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2ad6c-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="2ad6c-116">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="2ad6c-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2ad6c-117">T'</span><span class="sxs-lookup"><span data-stu-id="2ad6c-117">'T</span></span>

<span data-ttu-id="2ad6c-118">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="2ad6c-118">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="2ad6c-119">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="2ad6c-119">See Also</span></span>

- [<span data-ttu-id="2ad6c-120">Microsoft. Quantum. Canon. ApplyToElementC</span><span class="sxs-lookup"><span data-stu-id="2ad6c-120">Microsoft.Quantum.Canon.ApplyToElementC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementC)
- [<span data-ttu-id="2ad6c-121">Microsoft. Quantum. Canon. ApplyToElementA</span><span class="sxs-lookup"><span data-stu-id="2ad6c-121">Microsoft.Quantum.Canon.ApplyToElementA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementA)
- [<span data-ttu-id="2ad6c-122">Microsoft. Quantum. Canon. ApplyToElementCA</span><span class="sxs-lookup"><span data-stu-id="2ad6c-122">Microsoft.Quantum.Canon.ApplyToElementCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementCA)