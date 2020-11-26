---
uid: Microsoft.Quantum.Canon.RepeatCA
title: Operação RepeatCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatCA
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 24606486b3d5703065a7c7f62d3bbc7e3d07615f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205398"
---
# <a name="repeatca-operation"></a><span data-ttu-id="072ac-102">Operação RepeatCA</span><span class="sxs-lookup"><span data-stu-id="072ac-102">RepeatCA operation</span></span>

<span data-ttu-id="072ac-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="072ac-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="072ac-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="072ac-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="072ac-105">Repete uma operação um determinado número de vezes.</span><span class="sxs-lookup"><span data-stu-id="072ac-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation RepeatCA<'TInput> (op : ('TInput => Unit is Adj + Ctl), nTimes : Int, input : 'TInput) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="072ac-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="072ac-106">Input</span></span>

### <a name="op--tinput--unit--is-adj--ctl"></a><span data-ttu-id="072ac-107">op: a [unidade](xref:microsoft.quantum.lang-ref.unit)  ' TInput => é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="072ac-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="072ac-108">A operação a ser chamada repetidamente.</span><span class="sxs-lookup"><span data-stu-id="072ac-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="072ac-109">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="072ac-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="072ac-110">O número de vezes para chamar `op` .</span><span class="sxs-lookup"><span data-stu-id="072ac-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="072ac-111">entrada: ' TInput</span><span class="sxs-lookup"><span data-stu-id="072ac-111">input : 'TInput</span></span>

<span data-ttu-id="072ac-112">A entrada a ser passada para `op` .</span><span class="sxs-lookup"><span data-stu-id="072ac-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="072ac-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="072ac-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="072ac-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="072ac-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="072ac-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="072ac-115">'TInput</span></span>



## <a name="see-also"></a><span data-ttu-id="072ac-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="072ac-116">See Also</span></span>

- [<span data-ttu-id="072ac-117">Microsoft. Quantum. arrays. DrawMany</span><span class="sxs-lookup"><span data-stu-id="072ac-117">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="072ac-118">Microsoft. Quantum. Canon. Repeat</span><span class="sxs-lookup"><span data-stu-id="072ac-118">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)
- [<span data-ttu-id="072ac-119">Microsoft. Quantum. Canon. REPEATA</span><span class="sxs-lookup"><span data-stu-id="072ac-119">Microsoft.Quantum.Canon.RepeatA</span></span>](xref:Microsoft.Quantum.Canon.RepeatA)
- [<span data-ttu-id="072ac-120">Microsoft. Quantum. Canon. RepeatC</span><span class="sxs-lookup"><span data-stu-id="072ac-120">Microsoft.Quantum.Canon.RepeatC</span></span>](xref:Microsoft.Quantum.Canon.RepeatC)