---
uid: Microsoft.Quantum.Canon.ApplyToMost
title: Operação ApplyToMost
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMost
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: 7e7824b431ccff644cf5cc53145163327eb8ad36
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208526"
---
# <a name="applytomost-operation"></a><span data-ttu-id="85947-102">Operação ApplyToMost</span><span class="sxs-lookup"><span data-stu-id="85947-102">ApplyToMost operation</span></span>

<span data-ttu-id="85947-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="85947-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="85947-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="85947-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="85947-105">Aplica uma operação a todos, exceto ao último elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="85947-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMost<'T> (op : ('T[] => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="85947-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="85947-106">Description</span></span>

<span data-ttu-id="85947-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="85947-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="85947-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="85947-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="85947-109">op: ' t [] = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="85947-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="85947-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="85947-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="85947-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="85947-111">targets : 'T[]</span></span>

<span data-ttu-id="85947-112">Uma matriz de destinos, das quais todos, exceto o último, será aplicado `op` .</span><span class="sxs-lookup"><span data-stu-id="85947-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="85947-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="85947-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="85947-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="85947-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="85947-115">T'</span><span class="sxs-lookup"><span data-stu-id="85947-115">'T</span></span>

<span data-ttu-id="85947-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="85947-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="85947-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="85947-117">See Also</span></span>

- [<span data-ttu-id="85947-118">Microsoft. Quantum. Canon. ApplyToMostA</span><span class="sxs-lookup"><span data-stu-id="85947-118">Microsoft.Quantum.Canon.ApplyToMostA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostA)
- [<span data-ttu-id="85947-119">Microsoft. Quantum. Canon. ApplyToMostC</span><span class="sxs-lookup"><span data-stu-id="85947-119">Microsoft.Quantum.Canon.ApplyToMostC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostC)
- [<span data-ttu-id="85947-120">Microsoft. Quantum. Canon. ApplyToMostCA</span><span class="sxs-lookup"><span data-stu-id="85947-120">Microsoft.Quantum.Canon.ApplyToMostCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostCA)