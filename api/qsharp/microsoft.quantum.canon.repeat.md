---
uid: Microsoft.Quantum.Canon.Repeat
title: Repetir operação
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Repeat
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: cd572e5e082df94d762a0869ad2c1923fb71fd3d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205585"
---
# <a name="repeat-operation"></a><span data-ttu-id="f14c5-102">Repetir operação</span><span class="sxs-lookup"><span data-stu-id="f14c5-102">Repeat operation</span></span>

<span data-ttu-id="f14c5-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f14c5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f14c5-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f14c5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f14c5-105">Repete uma operação um determinado número de vezes.</span><span class="sxs-lookup"><span data-stu-id="f14c5-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation Repeat<'TInput> (op : ('TInput => Unit), nTimes : Int, input : 'TInput) : Unit
```


## <a name="input"></a><span data-ttu-id="f14c5-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="f14c5-106">Input</span></span>

### <a name="op--tinput--unit"></a><span data-ttu-id="f14c5-107">op: ' TInput = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="f14c5-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="f14c5-108">A operação a ser chamada repetidamente.</span><span class="sxs-lookup"><span data-stu-id="f14c5-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="f14c5-109">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f14c5-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f14c5-110">O número de vezes para chamar `op` .</span><span class="sxs-lookup"><span data-stu-id="f14c5-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="f14c5-111">entrada: ' TInput</span><span class="sxs-lookup"><span data-stu-id="f14c5-111">input : 'TInput</span></span>

<span data-ttu-id="f14c5-112">A entrada a ser passada para `op` .</span><span class="sxs-lookup"><span data-stu-id="f14c5-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f14c5-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f14c5-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f14c5-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="f14c5-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="f14c5-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="f14c5-115">'TInput</span></span>



## <a name="see-also"></a><span data-ttu-id="f14c5-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="f14c5-116">See Also</span></span>

- [<span data-ttu-id="f14c5-117">Microsoft. Quantum. arrays. DrawMany</span><span class="sxs-lookup"><span data-stu-id="f14c5-117">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="f14c5-118">Microsoft. Quantum. Canon. REPEATA</span><span class="sxs-lookup"><span data-stu-id="f14c5-118">Microsoft.Quantum.Canon.RepeatA</span></span>](xref:Microsoft.Quantum.Canon.RepeatA)
- [<span data-ttu-id="f14c5-119">Microsoft. Quantum. Canon. RepeatC</span><span class="sxs-lookup"><span data-stu-id="f14c5-119">Microsoft.Quantum.Canon.RepeatC</span></span>](xref:Microsoft.Quantum.Canon.RepeatC)
- [<span data-ttu-id="f14c5-120">Microsoft. Quantum. Canon. RepeatCA</span><span class="sxs-lookup"><span data-stu-id="f14c5-120">Microsoft.Quantum.Canon.RepeatCA</span></span>](xref:Microsoft.Quantum.Canon.RepeatCA)