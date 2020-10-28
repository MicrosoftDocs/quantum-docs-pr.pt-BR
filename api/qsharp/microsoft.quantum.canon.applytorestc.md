---
uid: Microsoft.Quantum.Canon.ApplyToRestC
title: Operação ApplyToRestC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRestC
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: 55e534b7b7673f300b607a8213418c45c8c7c92c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694140"
---
# <a name="applytorestc-operation"></a><span data-ttu-id="56a58-102">Operação ApplyToRestC</span><span class="sxs-lookup"><span data-stu-id="56a58-102">ApplyToRestC operation</span></span>

<span data-ttu-id="56a58-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="56a58-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="56a58-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="56a58-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="56a58-105">Aplica uma operação a todos, exceto ao primeiro elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="56a58-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRestC<'T> (op : ('T[] => Unit is Ctl), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="56a58-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="56a58-106">Description</span></span>

<span data-ttu-id="56a58-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="56a58-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="56a58-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="56a58-108">Input</span></span>

### <a name="op--t--unit-ctl"></a><span data-ttu-id="56a58-109">op: ' t [] => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="56a58-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="56a58-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="56a58-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="56a58-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="56a58-111">targets : 'T[]</span></span>

<span data-ttu-id="56a58-112">Uma matriz de destinos, das quais todos, exceto o primeiro, será aplicado `op` .</span><span class="sxs-lookup"><span data-stu-id="56a58-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="56a58-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="56a58-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="56a58-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="56a58-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="56a58-115">T'</span><span class="sxs-lookup"><span data-stu-id="56a58-115">'T</span></span>

<span data-ttu-id="56a58-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="56a58-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="56a58-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="56a58-117">See Also</span></span>

- [<span data-ttu-id="56a58-118">Microsoft. Quantum. Canon. ApplyToRest</span><span class="sxs-lookup"><span data-stu-id="56a58-118">Microsoft.Quantum.Canon.ApplyToRest</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRest)
- [<span data-ttu-id="56a58-119">Microsoft. Quantum. Canon. ApplyToRestA</span><span class="sxs-lookup"><span data-stu-id="56a58-119">Microsoft.Quantum.Canon.ApplyToRestA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestA)
- [<span data-ttu-id="56a58-120">Microsoft. Quantum. Canon. ApplyToRestCA</span><span class="sxs-lookup"><span data-stu-id="56a58-120">Microsoft.Quantum.Canon.ApplyToRestCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestCA)