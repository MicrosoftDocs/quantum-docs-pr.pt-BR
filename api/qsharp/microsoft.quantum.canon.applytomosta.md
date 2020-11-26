---
uid: Microsoft.Quantum.Canon.ApplyToMostA
title: Operação ApplyToMostA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostA
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: 7c226de9b2c99d124c467175dfe65a60a89d4332
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208492"
---
# <a name="applytomosta-operation"></a><span data-ttu-id="f03ce-102">Operação ApplyToMostA</span><span class="sxs-lookup"><span data-stu-id="f03ce-102">ApplyToMostA operation</span></span>

<span data-ttu-id="f03ce-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f03ce-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f03ce-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f03ce-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f03ce-105">Aplica uma operação a todos, exceto ao último elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="f03ce-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMostA<'T> (op : ('T[] => Unit is Adj), targets : 'T[]) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="f03ce-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="f03ce-106">Description</span></span>

<span data-ttu-id="f03ce-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="f03ce-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="f03ce-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="f03ce-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="f03ce-109">op: ' t [] = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="f03ce-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="f03ce-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="f03ce-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="f03ce-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="f03ce-111">targets : 'T[]</span></span>

<span data-ttu-id="f03ce-112">Uma matriz de destinos, das quais todos, exceto o último, será aplicado `op` .</span><span class="sxs-lookup"><span data-stu-id="f03ce-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f03ce-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f03ce-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f03ce-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="f03ce-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f03ce-115">T'</span><span class="sxs-lookup"><span data-stu-id="f03ce-115">'T</span></span>

<span data-ttu-id="f03ce-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="f03ce-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="f03ce-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="f03ce-117">See Also</span></span>

- [<span data-ttu-id="f03ce-118">Microsoft. Quantum. Canon. ApplyToMost</span><span class="sxs-lookup"><span data-stu-id="f03ce-118">Microsoft.Quantum.Canon.ApplyToMost</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [<span data-ttu-id="f03ce-119">Microsoft. Quantum. Canon. ApplyToMostC</span><span class="sxs-lookup"><span data-stu-id="f03ce-119">Microsoft.Quantum.Canon.ApplyToMostC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostC)
- [<span data-ttu-id="f03ce-120">Microsoft. Quantum. Canon. ApplyToMostCA</span><span class="sxs-lookup"><span data-stu-id="f03ce-120">Microsoft.Quantum.Canon.ApplyToMostCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostCA)