---
uid: Microsoft.Quantum.Canon.ApplyToMost
title: Operação ApplyToMost
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMost
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: a3918233e101f3d8956601dcc7d85edcf6196ac7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850601"
---
# <a name="applytomost-operation"></a><span data-ttu-id="e6021-102">Operação ApplyToMost</span><span class="sxs-lookup"><span data-stu-id="e6021-102">ApplyToMost operation</span></span>

<span data-ttu-id="e6021-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e6021-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e6021-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e6021-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e6021-105">Aplica uma operação a todos, exceto ao último elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="e6021-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMost<'T> (op : ('T[] => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="e6021-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="e6021-106">Description</span></span>

<span data-ttu-id="e6021-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="e6021-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="e6021-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="e6021-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="e6021-109">op: ' t [] = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="e6021-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="e6021-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="e6021-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="e6021-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="e6021-111">targets : 'T[]</span></span>

<span data-ttu-id="e6021-112">Uma matriz de destinos, das quais todos, exceto o último, será aplicado `op` .</span><span class="sxs-lookup"><span data-stu-id="e6021-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e6021-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e6021-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e6021-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="e6021-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e6021-115">T'</span><span class="sxs-lookup"><span data-stu-id="e6021-115">'T</span></span>

<span data-ttu-id="e6021-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="e6021-116">The input type of the operation to be applied.</span></span>

## <a name="example"></a><span data-ttu-id="e6021-117">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e6021-117">Example</span></span>

<span data-ttu-id="e6021-118">Os seguintes trechos de código Q # são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="e6021-118">The following Q# snippets are equivalent:</span></span>

```qsharp
ApplyToMost(ApplyCNOTChain, register);
ApplyCNOTChain(Most(register));
```

## <a name="see-also"></a><span data-ttu-id="e6021-119">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e6021-119">See Also</span></span>

- [<span data-ttu-id="e6021-120">Microsoft. Quantum. Canon. ApplyToMostA</span><span class="sxs-lookup"><span data-stu-id="e6021-120">Microsoft.Quantum.Canon.ApplyToMostA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostA)
- [<span data-ttu-id="e6021-121">Microsoft. Quantum. Canon. ApplyToMostC</span><span class="sxs-lookup"><span data-stu-id="e6021-121">Microsoft.Quantum.Canon.ApplyToMostC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostC)
- [<span data-ttu-id="e6021-122">Microsoft. Quantum. Canon. ApplyToMostCA</span><span class="sxs-lookup"><span data-stu-id="e6021-122">Microsoft.Quantum.Canon.ApplyToMostCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostCA)