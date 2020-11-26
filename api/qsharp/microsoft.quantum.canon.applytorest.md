---
uid: Microsoft.Quantum.Canon.ApplyToRest
title: Operação ApplyToRest
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRest
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: fe49361f3c2259960eaa58d47df9b69b30b572a8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208254"
---
# <a name="applytorest-operation"></a><span data-ttu-id="b2fc8-102">Operação ApplyToRest</span><span class="sxs-lookup"><span data-stu-id="b2fc8-102">ApplyToRest operation</span></span>

<span data-ttu-id="b2fc8-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b2fc8-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b2fc8-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b2fc8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b2fc8-105">Aplica uma operação a todos, exceto ao primeiro elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="b2fc8-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRest<'T> (op : ('T[] => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="b2fc8-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="b2fc8-106">Description</span></span>

<span data-ttu-id="b2fc8-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="b2fc8-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="b2fc8-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="b2fc8-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="b2fc8-109">op: ' t [] = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="b2fc8-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="b2fc8-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="b2fc8-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="b2fc8-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="b2fc8-111">targets : 'T[]</span></span>

<span data-ttu-id="b2fc8-112">Uma matriz de destinos, das quais todos, exceto o primeiro, será aplicado `op` .</span><span class="sxs-lookup"><span data-stu-id="b2fc8-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b2fc8-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b2fc8-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="b2fc8-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="b2fc8-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b2fc8-115">T'</span><span class="sxs-lookup"><span data-stu-id="b2fc8-115">'T</span></span>

<span data-ttu-id="b2fc8-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="b2fc8-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="b2fc8-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="b2fc8-117">See Also</span></span>

- [<span data-ttu-id="b2fc8-118">Microsoft. Quantum. Canon. ApplyToRestA</span><span class="sxs-lookup"><span data-stu-id="b2fc8-118">Microsoft.Quantum.Canon.ApplyToRestA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestA)
- [<span data-ttu-id="b2fc8-119">Microsoft. Quantum. Canon. ApplyToRestC</span><span class="sxs-lookup"><span data-stu-id="b2fc8-119">Microsoft.Quantum.Canon.ApplyToRestC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestC)
- [<span data-ttu-id="b2fc8-120">Microsoft. Quantum. Canon. ApplyToRestCA</span><span class="sxs-lookup"><span data-stu-id="b2fc8-120">Microsoft.Quantum.Canon.ApplyToRestCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestCA)