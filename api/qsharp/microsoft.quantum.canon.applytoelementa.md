---
uid: Microsoft.Quantum.Canon.ApplyToElementA
title: Operação ApplyToElementA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElementA
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: f34089c2a45de281507cb79bde8a8cb9d2fefe47
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694196"
---
# <a name="applytoelementa-operation"></a><span data-ttu-id="2a252-102">Operação ApplyToElementA</span><span class="sxs-lookup"><span data-stu-id="2a252-102">ApplyToElementA operation</span></span>

<span data-ttu-id="2a252-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="2a252-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="2a252-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2a252-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2a252-105">Aplica uma operação a um determinado elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="2a252-105">Applies an operation to a given element of an array.</span></span>

```qsharp
operation ApplyToElementA<'T> (op : ('T => Unit is Adj), index : Int, targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="2a252-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="2a252-106">Description</span></span>

<span data-ttu-id="2a252-107">Dada uma operação `op` , um índice `index` e uma matriz de destinos `targets` , aplicam-se `op(targets[index])` .</span><span class="sxs-lookup"><span data-stu-id="2a252-107">Given an operation `op`, an index `index`, and an array of targets `targets`, applies `op(targets[index])`.</span></span>

## <a name="input"></a><span data-ttu-id="2a252-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="2a252-108">Input</span></span>

### <a name="op--t--unit-adj"></a><span data-ttu-id="2a252-109">op: ' t => adj de [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2a252-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="2a252-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="2a252-110">An operation to be applied.</span></span>


### <a name="index--int"></a><span data-ttu-id="2a252-111">índice: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2a252-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2a252-112">Um índice na matriz de destinos.</span><span class="sxs-lookup"><span data-stu-id="2a252-112">An index into the array of targets.</span></span>


### <a name="targets--t"></a><span data-ttu-id="2a252-113">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="2a252-113">targets : 'T[]</span></span>

<span data-ttu-id="2a252-114">Uma matriz de possíveis destinos para `op` .</span><span class="sxs-lookup"><span data-stu-id="2a252-114">An array of possible targets for `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2a252-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2a252-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="2a252-116">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="2a252-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2a252-117">T'</span><span class="sxs-lookup"><span data-stu-id="2a252-117">'T</span></span>

<span data-ttu-id="2a252-118">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="2a252-118">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="2a252-119">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="2a252-119">See Also</span></span>

- [<span data-ttu-id="2a252-120">Microsoft. Quantum. Canon. ApplyToElement</span><span class="sxs-lookup"><span data-stu-id="2a252-120">Microsoft.Quantum.Canon.ApplyToElement</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElement)
- [<span data-ttu-id="2a252-121">Microsoft. Quantum. Canon. ApplyToElementC</span><span class="sxs-lookup"><span data-stu-id="2a252-121">Microsoft.Quantum.Canon.ApplyToElementC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementC)
- [<span data-ttu-id="2a252-122">Microsoft. Quantum. Canon. ApplyToElementCA</span><span class="sxs-lookup"><span data-stu-id="2a252-122">Microsoft.Quantum.Canon.ApplyToElementCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementCA)