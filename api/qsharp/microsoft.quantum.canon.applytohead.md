---
uid: Microsoft.Quantum.Canon.ApplyToHead
title: Operação ApplyToHead
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHead
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 4e5fc439f48a5c7e527b7805c35cce18eca3ab36
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694165"
---
# <a name="applytohead-operation"></a><span data-ttu-id="0d028-102">Operação ApplyToHead</span><span class="sxs-lookup"><span data-stu-id="0d028-102">ApplyToHead operation</span></span>

<span data-ttu-id="0d028-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0d028-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0d028-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0d028-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0d028-105">Aplica uma operação ao primeiro elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="0d028-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHead<'T> (op : ('T => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="0d028-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d028-106">Description</span></span>

<span data-ttu-id="0d028-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="0d028-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="0d028-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="0d028-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="0d028-109">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="0d028-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="0d028-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="0d028-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="0d028-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="0d028-111">targets : 'T[]</span></span>

<span data-ttu-id="0d028-112">Uma matriz de destinos, da qual a primeira será aplicada `op` .</span><span class="sxs-lookup"><span data-stu-id="0d028-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0d028-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0d028-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="0d028-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="0d028-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0d028-115">T'</span><span class="sxs-lookup"><span data-stu-id="0d028-115">'T</span></span>

<span data-ttu-id="0d028-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="0d028-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="0d028-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="0d028-117">See Also</span></span>

- [<span data-ttu-id="0d028-118">Microsoft. Quantum. Canon. ApplyToHeadA</span><span class="sxs-lookup"><span data-stu-id="0d028-118">Microsoft.Quantum.Canon.ApplyToHeadA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [<span data-ttu-id="0d028-119">Microsoft. Quantum. Canon. ApplyToHeadC</span><span class="sxs-lookup"><span data-stu-id="0d028-119">Microsoft.Quantum.Canon.ApplyToHeadC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadC)
- [<span data-ttu-id="0d028-120">Microsoft. Quantum. Canon. ApplyToHeadCA</span><span class="sxs-lookup"><span data-stu-id="0d028-120">Microsoft.Quantum.Canon.ApplyToHeadCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)