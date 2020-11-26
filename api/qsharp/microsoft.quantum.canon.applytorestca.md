---
uid: Microsoft.Quantum.Canon.ApplyToRestCA
title: Operação ApplyToRestCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRestCA
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: 3123c7f7b5e5c7f5cb17a34eedc81b3912109883
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208152"
---
# <a name="applytorestca-operation"></a><span data-ttu-id="baedd-102">Operação ApplyToRestCA</span><span class="sxs-lookup"><span data-stu-id="baedd-102">ApplyToRestCA operation</span></span>

<span data-ttu-id="baedd-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="baedd-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="baedd-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="baedd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="baedd-105">Aplica uma operação a todos, exceto ao primeiro elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="baedd-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRestCA<'T> (op : ('T[] => Unit is Adj + Ctl), targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="baedd-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="baedd-106">Description</span></span>

<span data-ttu-id="baedd-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="baedd-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="baedd-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="baedd-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="baedd-109">op: ' t [] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="baedd-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="baedd-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="baedd-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="baedd-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="baedd-111">targets : 'T[]</span></span>

<span data-ttu-id="baedd-112">Uma matriz de destinos, das quais todos, exceto o primeiro, será aplicado `op` .</span><span class="sxs-lookup"><span data-stu-id="baedd-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="baedd-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="baedd-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="baedd-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="baedd-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="baedd-115">T'</span><span class="sxs-lookup"><span data-stu-id="baedd-115">'T</span></span>

<span data-ttu-id="baedd-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="baedd-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="baedd-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="baedd-117">See Also</span></span>

- [<span data-ttu-id="baedd-118">Microsoft. Quantum. Canon. ApplyToRest</span><span class="sxs-lookup"><span data-stu-id="baedd-118">Microsoft.Quantum.Canon.ApplyToRest</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRest)
- [<span data-ttu-id="baedd-119">Microsoft. Quantum. Canon. ApplyToRestA</span><span class="sxs-lookup"><span data-stu-id="baedd-119">Microsoft.Quantum.Canon.ApplyToRestA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestA)
- [<span data-ttu-id="baedd-120">Microsoft. Quantum. Canon. ApplyToRestC</span><span class="sxs-lookup"><span data-stu-id="baedd-120">Microsoft.Quantum.Canon.ApplyToRestC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestC)