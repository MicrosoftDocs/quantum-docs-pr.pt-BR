---
uid: Microsoft.Quantum.Canon.ApplyToMostC
title: Operação ApplyToMostC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostC
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: a5927f6b296dd50afec8979c8e8ac22979b8a082
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694151"
---
# <a name="applytomostc-operation"></a><span data-ttu-id="5fca9-102">Operação ApplyToMostC</span><span class="sxs-lookup"><span data-stu-id="5fca9-102">ApplyToMostC operation</span></span>

<span data-ttu-id="5fca9-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5fca9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5fca9-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5fca9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5fca9-105">Aplica uma operação a todos, exceto ao último elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="5fca9-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMostC<'T> (op : ('T[] => Unit is Ctl), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="5fca9-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="5fca9-106">Description</span></span>

<span data-ttu-id="5fca9-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="5fca9-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="5fca9-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="5fca9-108">Input</span></span>

### <a name="op--t--unit-ctl"></a><span data-ttu-id="5fca9-109">op: ' t [] => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5fca9-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="5fca9-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="5fca9-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="5fca9-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="5fca9-111">targets : 'T[]</span></span>

<span data-ttu-id="5fca9-112">Uma matriz de destinos, das quais todos, exceto o último, será aplicado `op` .</span><span class="sxs-lookup"><span data-stu-id="5fca9-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5fca9-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5fca9-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="5fca9-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="5fca9-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5fca9-115">T'</span><span class="sxs-lookup"><span data-stu-id="5fca9-115">'T</span></span>

<span data-ttu-id="5fca9-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="5fca9-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="5fca9-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="5fca9-117">See Also</span></span>

- [<span data-ttu-id="5fca9-118">Microsoft. Quantum. Canon. ApplyToMost</span><span class="sxs-lookup"><span data-stu-id="5fca9-118">Microsoft.Quantum.Canon.ApplyToMost</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [<span data-ttu-id="5fca9-119">Microsoft. Quantum. Canon. ApplyToMostA</span><span class="sxs-lookup"><span data-stu-id="5fca9-119">Microsoft.Quantum.Canon.ApplyToMostA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostA)
- [<span data-ttu-id="5fca9-120">Microsoft. Quantum. Canon. ApplyToMostCA</span><span class="sxs-lookup"><span data-stu-id="5fca9-120">Microsoft.Quantum.Canon.ApplyToMostCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostCA)