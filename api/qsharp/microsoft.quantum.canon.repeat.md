---
uid: Microsoft.Quantum.Canon.Repeat
title: Repetir operação
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Repeat
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 5aedd056b851b8d8d7c25a32eb22587292e132a8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693926"
---
# <a name="repeat-operation"></a><span data-ttu-id="55a98-102">Repetir operação</span><span class="sxs-lookup"><span data-stu-id="55a98-102">Repeat operation</span></span>

<span data-ttu-id="55a98-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="55a98-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="55a98-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="55a98-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="55a98-105">Repete uma operação um determinado número de vezes.</span><span class="sxs-lookup"><span data-stu-id="55a98-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation Repeat<'TInput> (op : ('TInput => Unit), nTimes : Int, input : 'TInput) : Unit
```


## <a name="input"></a><span data-ttu-id="55a98-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="55a98-106">Input</span></span>

### <a name="op--tinput--unit"></a><span data-ttu-id="55a98-107">op: ' TInput = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="55a98-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="55a98-108">A operação a ser chamada repetidamente.</span><span class="sxs-lookup"><span data-stu-id="55a98-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="55a98-109">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="55a98-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="55a98-110">O número de vezes para chamar `op` .</span><span class="sxs-lookup"><span data-stu-id="55a98-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="55a98-111">entrada: ' TInput</span><span class="sxs-lookup"><span data-stu-id="55a98-111">input : 'TInput</span></span>

<span data-ttu-id="55a98-112">A entrada a ser passada para `op` .</span><span class="sxs-lookup"><span data-stu-id="55a98-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="55a98-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="55a98-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="55a98-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="55a98-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="55a98-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="55a98-115">'TInput</span></span>



## <a name="see-also"></a><span data-ttu-id="55a98-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="55a98-116">See Also</span></span>

- [<span data-ttu-id="55a98-117">Microsoft. Quantum. arrays. DrawMany</span><span class="sxs-lookup"><span data-stu-id="55a98-117">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="55a98-118">Microsoft. Quantum. Canon. REPEATA</span><span class="sxs-lookup"><span data-stu-id="55a98-118">Microsoft.Quantum.Canon.RepeatA</span></span>](xref:Microsoft.Quantum.Canon.RepeatA)
- [<span data-ttu-id="55a98-119">Microsoft. Quantum. Canon. RepeatC</span><span class="sxs-lookup"><span data-stu-id="55a98-119">Microsoft.Quantum.Canon.RepeatC</span></span>](xref:Microsoft.Quantum.Canon.RepeatC)
- [<span data-ttu-id="55a98-120">Microsoft. Quantum. Canon. RepeatCA</span><span class="sxs-lookup"><span data-stu-id="55a98-120">Microsoft.Quantum.Canon.RepeatCA</span></span>](xref:Microsoft.Quantum.Canon.RepeatCA)