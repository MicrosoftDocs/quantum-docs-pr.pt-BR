---
uid: Microsoft.Quantum.Canon.ApplyToMostCA
title: Operação ApplyToMostCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostCA
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: 797cbd835446f31b2df60dbb184f888e6d0356aa
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694150"
---
# <a name="applytomostca-operation"></a><span data-ttu-id="088bb-102">Operação ApplyToMostCA</span><span class="sxs-lookup"><span data-stu-id="088bb-102">ApplyToMostCA operation</span></span>

<span data-ttu-id="088bb-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="088bb-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="088bb-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="088bb-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="088bb-105">Aplica uma operação a todos, exceto ao último elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="088bb-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMostCA<'T> (op : ('T[] => Unit is Adj + Ctl), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="088bb-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="088bb-106">Description</span></span>

<span data-ttu-id="088bb-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="088bb-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="088bb-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="088bb-108">Input</span></span>

### <a name="op--t--unit-adj--ctl"></a><span data-ttu-id="088bb-109">op: ' t [] => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL</span><span class="sxs-lookup"><span data-stu-id="088bb-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="088bb-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="088bb-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="088bb-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="088bb-111">targets : 'T[]</span></span>

<span data-ttu-id="088bb-112">Uma matriz de destinos, das quais todos, exceto o último, será aplicado `op` .</span><span class="sxs-lookup"><span data-stu-id="088bb-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="088bb-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="088bb-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="088bb-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="088bb-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="088bb-115">T'</span><span class="sxs-lookup"><span data-stu-id="088bb-115">'T</span></span>

<span data-ttu-id="088bb-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="088bb-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="088bb-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="088bb-117">See Also</span></span>

- [<span data-ttu-id="088bb-118">Microsoft. Quantum. Canon. ApplyToMost</span><span class="sxs-lookup"><span data-stu-id="088bb-118">Microsoft.Quantum.Canon.ApplyToMost</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [<span data-ttu-id="088bb-119">Microsoft. Quantum. Canon. ApplyToMostA</span><span class="sxs-lookup"><span data-stu-id="088bb-119">Microsoft.Quantum.Canon.ApplyToMostA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostA)
- [<span data-ttu-id="088bb-120">Microsoft. Quantum. Canon. ApplyToMostC</span><span class="sxs-lookup"><span data-stu-id="088bb-120">Microsoft.Quantum.Canon.ApplyToMostC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostC)