---
uid: Microsoft.Quantum.Canon.ApplyToHeadA
title: Operação ApplyToHeadA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHeadA
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 3397c059706c48ff8ca47dd2312cfa9565aacaba
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208628"
---
# <a name="applytoheada-operation"></a><span data-ttu-id="830f9-102">Operação ApplyToHeadA</span><span class="sxs-lookup"><span data-stu-id="830f9-102">ApplyToHeadA operation</span></span>

<span data-ttu-id="830f9-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="830f9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="830f9-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="830f9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="830f9-105">Aplica uma operação ao primeiro elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="830f9-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHeadA<'T> (op : ('T => Unit is Adj), targets : 'T[]) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="830f9-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="830f9-106">Description</span></span>

<span data-ttu-id="830f9-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="830f9-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="830f9-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="830f9-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="830f9-109">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="830f9-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="830f9-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="830f9-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="830f9-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="830f9-111">targets : 'T[]</span></span>

<span data-ttu-id="830f9-112">Uma matriz de destinos, da qual a primeira será aplicada `op` .</span><span class="sxs-lookup"><span data-stu-id="830f9-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="830f9-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="830f9-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="830f9-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="830f9-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="830f9-115">T'</span><span class="sxs-lookup"><span data-stu-id="830f9-115">'T</span></span>

<span data-ttu-id="830f9-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="830f9-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="830f9-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="830f9-117">See Also</span></span>

- [<span data-ttu-id="830f9-118">Microsoft. Quantum. Canon. ApplyToHead</span><span class="sxs-lookup"><span data-stu-id="830f9-118">Microsoft.Quantum.Canon.ApplyToHead</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHead)
- [<span data-ttu-id="830f9-119">Microsoft. Quantum. Canon. ApplyToHeadC</span><span class="sxs-lookup"><span data-stu-id="830f9-119">Microsoft.Quantum.Canon.ApplyToHeadC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadC)
- [<span data-ttu-id="830f9-120">Microsoft. Quantum. Canon. ApplyToHeadCA</span><span class="sxs-lookup"><span data-stu-id="830f9-120">Microsoft.Quantum.Canon.ApplyToHeadCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)