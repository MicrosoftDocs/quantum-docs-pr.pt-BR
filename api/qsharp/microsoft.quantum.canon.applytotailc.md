---
uid: Microsoft.Quantum.Canon.ApplyToTailC
title: Operação ApplyToTailC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTailC
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 5a68cae3fd122416cfd064e0078e03f5c00ab492
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217281"
---
# <a name="applytotailc-operation"></a><span data-ttu-id="79ce1-102">Operação ApplyToTailC</span><span class="sxs-lookup"><span data-stu-id="79ce1-102">ApplyToTailC operation</span></span>

<span data-ttu-id="79ce1-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="79ce1-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="79ce1-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="79ce1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="79ce1-105">Aplica uma operação ao último elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="79ce1-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTailC<'T> (op : ('T => Unit is Ctl), targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="79ce1-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="79ce1-106">Description</span></span>

<span data-ttu-id="79ce1-107">Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="79ce1-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="79ce1-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="79ce1-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="79ce1-109">op: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é CTL</span><span class="sxs-lookup"><span data-stu-id="79ce1-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="79ce1-110">Uma operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="79ce1-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="79ce1-111">destinos: ' t []</span><span class="sxs-lookup"><span data-stu-id="79ce1-111">targets : 'T[]</span></span>

<span data-ttu-id="79ce1-112">Uma matriz de destinos, da qual a última será aplicada `op` .</span><span class="sxs-lookup"><span data-stu-id="79ce1-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="79ce1-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="79ce1-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="79ce1-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="79ce1-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="79ce1-115">T'</span><span class="sxs-lookup"><span data-stu-id="79ce1-115">'T</span></span>

<span data-ttu-id="79ce1-116">O tipo de entrada da operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="79ce1-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="79ce1-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="79ce1-117">See Also</span></span>

- [<span data-ttu-id="79ce1-118">Microsoft. Quantum. Canon. ApplyToTail</span><span class="sxs-lookup"><span data-stu-id="79ce1-118">Microsoft.Quantum.Canon.ApplyToTail</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTail)
- [<span data-ttu-id="79ce1-119">Microsoft. Quantum. Canon. ApplyToTailA</span><span class="sxs-lookup"><span data-stu-id="79ce1-119">Microsoft.Quantum.Canon.ApplyToTailA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [<span data-ttu-id="79ce1-120">Microsoft. Quantum. Canon. ApplyToTailCA</span><span class="sxs-lookup"><span data-stu-id="79ce1-120">Microsoft.Quantum.Canon.ApplyToTailCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailCA)