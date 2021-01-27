---
uid: Microsoft.Quantum.Canon.ApplyToMostCA
title: Operação ApplyToMostCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostCA
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: 0a80c23e0c6ff45083c192579dd8301d2277cef2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841306"
---
# <a name="applytomostca-operation"></a><span data-ttu-id="4e5af-102">Operação ApplyToMostCA</span><span class="sxs-lookup"><span data-stu-id="4e5af-102">ApplyToMostCA operation</span></span>

<span data-ttu-id="4e5af-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="4e5af-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="4e5af-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4e5af-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4e5af-105">Aplica uma operação a todos, exceto ao último elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="4e5af-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMostCA<'T> (op : ('T[] => Unit is Adj + Ctl), targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="4e5af-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e5af-106">Description</span></span>

<span data-ttu-id="4e5af-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="4e5af-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="4e5af-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="4e5af-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="4e5af-109">op: ' t [] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="4e5af-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="4e5af-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="4e5af-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="4e5af-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="4e5af-111">targets : 'T[]</span></span>

<span data-ttu-id="4e5af-112">Uma matriz de destinos, das quais todos, exceto o último, será aplicado `op` .</span><span class="sxs-lookup"><span data-stu-id="4e5af-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4e5af-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4e5af-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="4e5af-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="4e5af-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4e5af-115">T'</span><span class="sxs-lookup"><span data-stu-id="4e5af-115">'T</span></span>

<span data-ttu-id="4e5af-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="4e5af-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="4e5af-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="4e5af-117">See Also</span></span>

- [<span data-ttu-id="4e5af-118">Microsoft. Quantum. Canon. ApplyToMost</span><span class="sxs-lookup"><span data-stu-id="4e5af-118">Microsoft.Quantum.Canon.ApplyToMost</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [<span data-ttu-id="4e5af-119">Microsoft. Quantum. Canon. ApplyToMostA</span><span class="sxs-lookup"><span data-stu-id="4e5af-119">Microsoft.Quantum.Canon.ApplyToMostA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostA)
- [<span data-ttu-id="4e5af-120">Microsoft. Quantum. Canon. ApplyToMostC</span><span class="sxs-lookup"><span data-stu-id="4e5af-120">Microsoft.Quantum.Canon.ApplyToMostC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostC)