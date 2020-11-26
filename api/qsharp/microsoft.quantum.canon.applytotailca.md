---
uid: Microsoft.Quantum.Canon.ApplyToTailCA
title: Operação ApplyToTailCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTailCA
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: afb9eaa277814d7434b00a5c853a0c002190c1ae
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207846"
---
# <a name="applytotailca-operation"></a><span data-ttu-id="a5ebd-102">Operação ApplyToTailCA</span><span class="sxs-lookup"><span data-stu-id="a5ebd-102">ApplyToTailCA operation</span></span>

<span data-ttu-id="a5ebd-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a5ebd-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a5ebd-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a5ebd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a5ebd-105">Aplica uma operação ao último elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="a5ebd-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTailCA<'T> (op : ('T => Unit is Adj + Ctl), targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="a5ebd-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="a5ebd-106">Description</span></span>

<span data-ttu-id="a5ebd-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="a5ebd-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="a5ebd-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="a5ebd-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="a5ebd-109">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="a5ebd-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="a5ebd-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="a5ebd-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="a5ebd-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="a5ebd-111">targets : 'T[]</span></span>

<span data-ttu-id="a5ebd-112">Uma matriz de destinos, da qual a última será aplicada `op` .</span><span class="sxs-lookup"><span data-stu-id="a5ebd-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a5ebd-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a5ebd-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a5ebd-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="a5ebd-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a5ebd-115">T'</span><span class="sxs-lookup"><span data-stu-id="a5ebd-115">'T</span></span>

<span data-ttu-id="a5ebd-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="a5ebd-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="a5ebd-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="a5ebd-117">See Also</span></span>

- [<span data-ttu-id="a5ebd-118">Microsoft. Quantum. Canon. ApplyToTail</span><span class="sxs-lookup"><span data-stu-id="a5ebd-118">Microsoft.Quantum.Canon.ApplyToTail</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTail)
- [<span data-ttu-id="a5ebd-119">Microsoft. Quantum. Canon. ApplyToTailA</span><span class="sxs-lookup"><span data-stu-id="a5ebd-119">Microsoft.Quantum.Canon.ApplyToTailA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [<span data-ttu-id="a5ebd-120">Microsoft. Quantum. Canon. ApplyToTailC</span><span class="sxs-lookup"><span data-stu-id="a5ebd-120">Microsoft.Quantum.Canon.ApplyToTailC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailC)