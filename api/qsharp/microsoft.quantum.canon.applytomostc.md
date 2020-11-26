---
uid: Microsoft.Quantum.Canon.ApplyToMostC
title: Operação ApplyToMostC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostC
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: af55093e44ce023c9e8b7e478730f4c527cf6d32
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208458"
---
# <a name="applytomostc-operation"></a><span data-ttu-id="d55b3-102">Operação ApplyToMostC</span><span class="sxs-lookup"><span data-stu-id="d55b3-102">ApplyToMostC operation</span></span>

<span data-ttu-id="d55b3-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d55b3-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d55b3-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d55b3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d55b3-105">Aplica uma operação a todos, exceto ao último elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="d55b3-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMostC<'T> (op : ('T[] => Unit is Ctl), targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="d55b3-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="d55b3-106">Description</span></span>

<span data-ttu-id="d55b3-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="d55b3-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="d55b3-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="d55b3-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="d55b3-109">op: ' t [] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é CTL</span><span class="sxs-lookup"><span data-stu-id="d55b3-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="d55b3-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="d55b3-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="d55b3-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="d55b3-111">targets : 'T[]</span></span>

<span data-ttu-id="d55b3-112">Uma matriz de destinos, das quais todos, exceto o último, será aplicado `op` .</span><span class="sxs-lookup"><span data-stu-id="d55b3-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d55b3-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d55b3-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d55b3-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="d55b3-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d55b3-115">T'</span><span class="sxs-lookup"><span data-stu-id="d55b3-115">'T</span></span>

<span data-ttu-id="d55b3-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="d55b3-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="d55b3-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d55b3-117">See Also</span></span>

- [<span data-ttu-id="d55b3-118">Microsoft. Quantum. Canon. ApplyToMost</span><span class="sxs-lookup"><span data-stu-id="d55b3-118">Microsoft.Quantum.Canon.ApplyToMost</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [<span data-ttu-id="d55b3-119">Microsoft. Quantum. Canon. ApplyToMostA</span><span class="sxs-lookup"><span data-stu-id="d55b3-119">Microsoft.Quantum.Canon.ApplyToMostA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostA)
- [<span data-ttu-id="d55b3-120">Microsoft. Quantum. Canon. ApplyToMostCA</span><span class="sxs-lookup"><span data-stu-id="d55b3-120">Microsoft.Quantum.Canon.ApplyToMostCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostCA)