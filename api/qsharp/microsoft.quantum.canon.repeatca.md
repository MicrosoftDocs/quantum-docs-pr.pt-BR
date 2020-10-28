---
uid: Microsoft.Quantum.Canon.RepeatCA
title: Operação RepeatCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatCA
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: b68c3aa4298fffa76f7c43ac4c6d27cdf3b72fbf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693919"
---
# <a name="repeatca-operation"></a><span data-ttu-id="bfaea-102">Operação RepeatCA</span><span class="sxs-lookup"><span data-stu-id="bfaea-102">RepeatCA operation</span></span>

<span data-ttu-id="bfaea-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="bfaea-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="bfaea-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bfaea-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bfaea-105">Repete uma operação um determinado número de vezes.</span><span class="sxs-lookup"><span data-stu-id="bfaea-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation RepeatCA<'TInput> (op : ('TInput => Unit is Adj + Ctl), nTimes : Int, input : 'TInput) : Unit
```


## <a name="input"></a><span data-ttu-id="bfaea-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="bfaea-106">Input</span></span>

### <a name="op--tinput--unit-adj--ctl"></a><span data-ttu-id="bfaea-107">op: ' TInput => [unidade](xref:microsoft.quantum.lang-ref.unit) do ano + CTL</span><span class="sxs-lookup"><span data-stu-id="bfaea-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="bfaea-108">A operação a ser chamada repetidamente.</span><span class="sxs-lookup"><span data-stu-id="bfaea-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="bfaea-109">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bfaea-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bfaea-110">O número de vezes para chamar `op` .</span><span class="sxs-lookup"><span data-stu-id="bfaea-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="bfaea-111">entrada: ' TInput</span><span class="sxs-lookup"><span data-stu-id="bfaea-111">input : 'TInput</span></span>

<span data-ttu-id="bfaea-112">A entrada a ser passada para `op` .</span><span class="sxs-lookup"><span data-stu-id="bfaea-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="bfaea-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bfaea-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="bfaea-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="bfaea-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="bfaea-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="bfaea-115">'TInput</span></span>



## <a name="see-also"></a><span data-ttu-id="bfaea-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="bfaea-116">See Also</span></span>

- [<span data-ttu-id="bfaea-117">Microsoft. Quantum. arrays. DrawMany</span><span class="sxs-lookup"><span data-stu-id="bfaea-117">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="bfaea-118">Microsoft. Quantum. Canon. Repeat</span><span class="sxs-lookup"><span data-stu-id="bfaea-118">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)
- [<span data-ttu-id="bfaea-119">Microsoft. Quantum. Canon. REPEATA</span><span class="sxs-lookup"><span data-stu-id="bfaea-119">Microsoft.Quantum.Canon.RepeatA</span></span>](xref:Microsoft.Quantum.Canon.RepeatA)
- [<span data-ttu-id="bfaea-120">Microsoft. Quantum. Canon. RepeatC</span><span class="sxs-lookup"><span data-stu-id="bfaea-120">Microsoft.Quantum.Canon.RepeatC</span></span>](xref:Microsoft.Quantum.Canon.RepeatC)