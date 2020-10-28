---
uid: Microsoft.Quantum.Canon.RepeatA
title: Operação REPEATA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatA
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 89d34e5a30a61dee392904ce1076605432e21395
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693921"
---
# <a name="repeata-operation"></a><span data-ttu-id="3605f-102">Operação REPEATA</span><span class="sxs-lookup"><span data-stu-id="3605f-102">RepeatA operation</span></span>

<span data-ttu-id="3605f-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="3605f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="3605f-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3605f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3605f-105">Repete uma operação um determinado número de vezes.</span><span class="sxs-lookup"><span data-stu-id="3605f-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation RepeatA<'TInput> (op : ('TInput => Unit is Adj), nTimes : Int, input : 'TInput) : Unit
```


## <a name="input"></a><span data-ttu-id="3605f-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="3605f-106">Input</span></span>

### <a name="op--tinput--unit-adj"></a><span data-ttu-id="3605f-107">op: ' TInput => adj da [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3605f-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="3605f-108">A operação a ser chamada repetidamente.</span><span class="sxs-lookup"><span data-stu-id="3605f-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="3605f-109">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3605f-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3605f-110">O número de vezes para chamar `op` .</span><span class="sxs-lookup"><span data-stu-id="3605f-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="3605f-111">entrada: ' TInput</span><span class="sxs-lookup"><span data-stu-id="3605f-111">input : 'TInput</span></span>

<span data-ttu-id="3605f-112">A entrada a ser passada para `op` .</span><span class="sxs-lookup"><span data-stu-id="3605f-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3605f-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3605f-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="3605f-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="3605f-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="3605f-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="3605f-115">'TInput</span></span>



## <a name="see-also"></a><span data-ttu-id="3605f-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="3605f-116">See Also</span></span>

- [<span data-ttu-id="3605f-117">Microsoft. Quantum. arrays. DrawMany</span><span class="sxs-lookup"><span data-stu-id="3605f-117">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="3605f-118">Microsoft. Quantum. Canon. Repeat</span><span class="sxs-lookup"><span data-stu-id="3605f-118">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)
- [<span data-ttu-id="3605f-119">Microsoft. Quantum. Canon. RepeatC</span><span class="sxs-lookup"><span data-stu-id="3605f-119">Microsoft.Quantum.Canon.RepeatC</span></span>](xref:Microsoft.Quantum.Canon.RepeatC)
- [<span data-ttu-id="3605f-120">Microsoft. Quantum. Canon. RepeatCA</span><span class="sxs-lookup"><span data-stu-id="3605f-120">Microsoft.Quantum.Canon.RepeatCA</span></span>](xref:Microsoft.Quantum.Canon.RepeatCA)