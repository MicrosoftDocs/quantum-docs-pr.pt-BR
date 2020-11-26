---
uid: Microsoft.Quantum.Canon.ApplyToHead
title: Operação ApplyToHead
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHead
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 35f19cbb1090e974e18f338239764c9c8b854116
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217332"
---
# <a name="applytohead-operation"></a><span data-ttu-id="df8a0-102">Operação ApplyToHead</span><span class="sxs-lookup"><span data-stu-id="df8a0-102">ApplyToHead operation</span></span>

<span data-ttu-id="df8a0-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="df8a0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="df8a0-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="df8a0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="df8a0-105">Aplica uma operação ao primeiro elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="df8a0-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHead<'T> (op : ('T => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="df8a0-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="df8a0-106">Description</span></span>

<span data-ttu-id="df8a0-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="df8a0-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="df8a0-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="df8a0-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="df8a0-109">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="df8a0-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="df8a0-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="df8a0-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="df8a0-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="df8a0-111">targets : 'T[]</span></span>

<span data-ttu-id="df8a0-112">Uma matriz de destinos, da qual a primeira será aplicada `op` .</span><span class="sxs-lookup"><span data-stu-id="df8a0-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="df8a0-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="df8a0-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="df8a0-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="df8a0-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="df8a0-115">T'</span><span class="sxs-lookup"><span data-stu-id="df8a0-115">'T</span></span>

<span data-ttu-id="df8a0-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="df8a0-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="df8a0-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="df8a0-117">See Also</span></span>

- [<span data-ttu-id="df8a0-118">Microsoft. Quantum. Canon. ApplyToHeadA</span><span class="sxs-lookup"><span data-stu-id="df8a0-118">Microsoft.Quantum.Canon.ApplyToHeadA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [<span data-ttu-id="df8a0-119">Microsoft. Quantum. Canon. ApplyToHeadC</span><span class="sxs-lookup"><span data-stu-id="df8a0-119">Microsoft.Quantum.Canon.ApplyToHeadC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadC)
- [<span data-ttu-id="df8a0-120">Microsoft. Quantum. Canon. ApplyToHeadCA</span><span class="sxs-lookup"><span data-stu-id="df8a0-120">Microsoft.Quantum.Canon.ApplyToHeadCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)