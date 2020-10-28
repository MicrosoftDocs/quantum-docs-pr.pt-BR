---
uid: Microsoft.Quantum.Canon.ApplyToHeadA
title: Operação ApplyToHeadA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHeadA
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: ba060243cb01782fd8529e0b05ee7258a66314f5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694163"
---
# <a name="applytoheada-operation"></a><span data-ttu-id="9bf4f-102">Operação ApplyToHeadA</span><span class="sxs-lookup"><span data-stu-id="9bf4f-102">ApplyToHeadA operation</span></span>

<span data-ttu-id="9bf4f-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9bf4f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9bf4f-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9bf4f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9bf4f-105">Aplica uma operação ao primeiro elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="9bf4f-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHeadA<'T> (op : ('T => Unit is Adj), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="9bf4f-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="9bf4f-106">Description</span></span>

<span data-ttu-id="9bf4f-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="9bf4f-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="9bf4f-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="9bf4f-108">Input</span></span>

### <a name="op--t--unit-adj"></a><span data-ttu-id="9bf4f-109">op: ' t => adj de [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9bf4f-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="9bf4f-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="9bf4f-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="9bf4f-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="9bf4f-111">targets : 'T[]</span></span>

<span data-ttu-id="9bf4f-112">Uma matriz de destinos, da qual a primeira será aplicada `op` .</span><span class="sxs-lookup"><span data-stu-id="9bf4f-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9bf4f-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9bf4f-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="9bf4f-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="9bf4f-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9bf4f-115">T'</span><span class="sxs-lookup"><span data-stu-id="9bf4f-115">'T</span></span>

<span data-ttu-id="9bf4f-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="9bf4f-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="9bf4f-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="9bf4f-117">See Also</span></span>

- [<span data-ttu-id="9bf4f-118">Microsoft. Quantum. Canon. ApplyToHead</span><span class="sxs-lookup"><span data-stu-id="9bf4f-118">Microsoft.Quantum.Canon.ApplyToHead</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHead)
- [<span data-ttu-id="9bf4f-119">Microsoft. Quantum. Canon. ApplyToHeadC</span><span class="sxs-lookup"><span data-stu-id="9bf4f-119">Microsoft.Quantum.Canon.ApplyToHeadC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadC)
- [<span data-ttu-id="9bf4f-120">Microsoft. Quantum. Canon. ApplyToHeadCA</span><span class="sxs-lookup"><span data-stu-id="9bf4f-120">Microsoft.Quantum.Canon.ApplyToHeadCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)