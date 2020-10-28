---
uid: Microsoft.Quantum.Canon.ApplyToRestCA
title: Operação ApplyToRestCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRestCA
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: d2dc10803044980d53f80f0577d16cb14a2eb301
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694136"
---
# <a name="applytorestca-operation"></a><span data-ttu-id="20484-102">Operação ApplyToRestCA</span><span class="sxs-lookup"><span data-stu-id="20484-102">ApplyToRestCA operation</span></span>

<span data-ttu-id="20484-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="20484-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="20484-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="20484-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="20484-105">Aplica uma operação a todos, exceto ao primeiro elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="20484-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRestCA<'T> (op : ('T[] => Unit is Adj + Ctl), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="20484-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="20484-106">Description</span></span>

<span data-ttu-id="20484-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="20484-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="20484-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="20484-108">Input</span></span>

### <a name="op--t--unit-adj--ctl"></a><span data-ttu-id="20484-109">op: ' t [] => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL</span><span class="sxs-lookup"><span data-stu-id="20484-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="20484-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="20484-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="20484-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="20484-111">targets : 'T[]</span></span>

<span data-ttu-id="20484-112">Uma matriz de destinos, das quais todos, exceto o primeiro, será aplicado `op` .</span><span class="sxs-lookup"><span data-stu-id="20484-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="20484-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="20484-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="20484-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="20484-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="20484-115">T'</span><span class="sxs-lookup"><span data-stu-id="20484-115">'T</span></span>

<span data-ttu-id="20484-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="20484-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="20484-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="20484-117">See Also</span></span>

- [<span data-ttu-id="20484-118">Microsoft. Quantum. Canon. ApplyToRest</span><span class="sxs-lookup"><span data-stu-id="20484-118">Microsoft.Quantum.Canon.ApplyToRest</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRest)
- [<span data-ttu-id="20484-119">Microsoft. Quantum. Canon. ApplyToRestA</span><span class="sxs-lookup"><span data-stu-id="20484-119">Microsoft.Quantum.Canon.ApplyToRestA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestA)
- [<span data-ttu-id="20484-120">Microsoft. Quantum. Canon. ApplyToRestC</span><span class="sxs-lookup"><span data-stu-id="20484-120">Microsoft.Quantum.Canon.ApplyToRestC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestC)