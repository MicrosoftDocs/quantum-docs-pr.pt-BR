---
uid: Microsoft.Quantum.Canon.RepeatC
title: Operação RepeatC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatC
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 8dc178374bdc9f8bf9f8aed57b9ae9a56995dec6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693920"
---
# <a name="repeatc-operation"></a><span data-ttu-id="06d15-102">Operação RepeatC</span><span class="sxs-lookup"><span data-stu-id="06d15-102">RepeatC operation</span></span>

<span data-ttu-id="06d15-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="06d15-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="06d15-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="06d15-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="06d15-105">Repete uma operação um determinado número de vezes.</span><span class="sxs-lookup"><span data-stu-id="06d15-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation RepeatC<'TInput> (op : ('TInput => Unit is Ctl), nTimes : Int, input : 'TInput) : Unit
```


## <a name="input"></a><span data-ttu-id="06d15-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="06d15-106">Input</span></span>

### <a name="op--tinput--unit-ctl"></a><span data-ttu-id="06d15-107">op: ' TInput => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="06d15-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="06d15-108">A operação a ser chamada repetidamente.</span><span class="sxs-lookup"><span data-stu-id="06d15-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="06d15-109">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="06d15-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="06d15-110">O número de vezes para chamar `op` .</span><span class="sxs-lookup"><span data-stu-id="06d15-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="06d15-111">entrada: ' TInput</span><span class="sxs-lookup"><span data-stu-id="06d15-111">input : 'TInput</span></span>

<span data-ttu-id="06d15-112">A entrada a ser passada para `op` .</span><span class="sxs-lookup"><span data-stu-id="06d15-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="06d15-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="06d15-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="06d15-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="06d15-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="06d15-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="06d15-115">'TInput</span></span>



## <a name="see-also"></a><span data-ttu-id="06d15-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="06d15-116">See Also</span></span>

- [<span data-ttu-id="06d15-117">Microsoft. Quantum. arrays. DrawMany</span><span class="sxs-lookup"><span data-stu-id="06d15-117">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="06d15-118">Microsoft. Quantum. Canon. Repeat</span><span class="sxs-lookup"><span data-stu-id="06d15-118">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)
- [<span data-ttu-id="06d15-119">Microsoft. Quantum. Canon. REPEATA</span><span class="sxs-lookup"><span data-stu-id="06d15-119">Microsoft.Quantum.Canon.RepeatA</span></span>](xref:Microsoft.Quantum.Canon.RepeatA)
- [<span data-ttu-id="06d15-120">Microsoft. Quantum. Canon. RepeatCA</span><span class="sxs-lookup"><span data-stu-id="06d15-120">Microsoft.Quantum.Canon.RepeatCA</span></span>](xref:Microsoft.Quantum.Canon.RepeatCA)