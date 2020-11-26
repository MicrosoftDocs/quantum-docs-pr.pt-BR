---
uid: Microsoft.Quantum.Canon.RepeatC
title: Operação RepeatC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatC
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 30fd172584b36601c4b81deff494cf55964518f2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205432"
---
# <a name="repeatc-operation"></a><span data-ttu-id="e681b-102">Operação RepeatC</span><span class="sxs-lookup"><span data-stu-id="e681b-102">RepeatC operation</span></span>

<span data-ttu-id="e681b-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e681b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e681b-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e681b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e681b-105">Repete uma operação um determinado número de vezes.</span><span class="sxs-lookup"><span data-stu-id="e681b-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation RepeatC<'TInput> (op : ('TInput => Unit is Ctl), nTimes : Int, input : 'TInput) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="e681b-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="e681b-106">Input</span></span>

### <a name="op--tinput--unit--is-ctl"></a><span data-ttu-id="e681b-107">op: a [unidade](xref:microsoft.quantum.lang-ref.unit)  ' TInput => é CTL</span><span class="sxs-lookup"><span data-stu-id="e681b-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="e681b-108">A operação a ser chamada repetidamente.</span><span class="sxs-lookup"><span data-stu-id="e681b-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="e681b-109">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e681b-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e681b-110">O número de vezes para chamar `op` .</span><span class="sxs-lookup"><span data-stu-id="e681b-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="e681b-111">entrada: ' TInput</span><span class="sxs-lookup"><span data-stu-id="e681b-111">input : 'TInput</span></span>

<span data-ttu-id="e681b-112">A entrada a ser passada para `op` .</span><span class="sxs-lookup"><span data-stu-id="e681b-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e681b-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e681b-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e681b-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="e681b-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="e681b-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="e681b-115">'TInput</span></span>



## <a name="see-also"></a><span data-ttu-id="e681b-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e681b-116">See Also</span></span>

- [<span data-ttu-id="e681b-117">Microsoft. Quantum. arrays. DrawMany</span><span class="sxs-lookup"><span data-stu-id="e681b-117">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="e681b-118">Microsoft. Quantum. Canon. Repeat</span><span class="sxs-lookup"><span data-stu-id="e681b-118">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)
- [<span data-ttu-id="e681b-119">Microsoft. Quantum. Canon. REPEATA</span><span class="sxs-lookup"><span data-stu-id="e681b-119">Microsoft.Quantum.Canon.RepeatA</span></span>](xref:Microsoft.Quantum.Canon.RepeatA)
- [<span data-ttu-id="e681b-120">Microsoft. Quantum. Canon. RepeatCA</span><span class="sxs-lookup"><span data-stu-id="e681b-120">Microsoft.Quantum.Canon.RepeatCA</span></span>](xref:Microsoft.Quantum.Canon.RepeatCA)