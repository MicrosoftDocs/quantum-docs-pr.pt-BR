---
uid: Microsoft.Quantum.Arrays.DrawMany
title: Operação DrawMany
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: DrawMany
qsharp.summary: Repeats an operation for a given number of samples, collecting its outputs in an array.
ms.openlocfilehash: 601fe603a869dcf977c1ceade5819ee64f634d53
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694493"
---
# <a name="drawmany-operation"></a><span data-ttu-id="bf6ec-102">Operação DrawMany</span><span class="sxs-lookup"><span data-stu-id="bf6ec-102">DrawMany operation</span></span>

<span data-ttu-id="bf6ec-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="bf6ec-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="bf6ec-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bf6ec-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bf6ec-105">Repete uma operação para um determinado número de amostras, coletando suas saídas em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="bf6ec-105">Repeats an operation for a given number of samples, collecting its outputs in an array.</span></span>

```qsharp
operation DrawMany<'TInput, 'TOutput> (op : ('TInput => 'TOutput), nSamples : Int, input : 'TInput) : 'TOutput[]
```


## <a name="input"></a><span data-ttu-id="bf6ec-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="bf6ec-106">Input</span></span>

### <a name="op--tinput--toutput"></a><span data-ttu-id="bf6ec-107">op: ' TInput => ' TOutput</span><span class="sxs-lookup"><span data-stu-id="bf6ec-107">op : 'TInput => 'TOutput</span></span> 

<span data-ttu-id="bf6ec-108">A operação a ser chamada repetidamente.</span><span class="sxs-lookup"><span data-stu-id="bf6ec-108">The operation to be called repeatedly.</span></span>


### <a name="nsamples--int"></a><span data-ttu-id="bf6ec-109">nSamples: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bf6ec-109">nSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bf6ec-110">O número de amostras de chamada `op` para Collect.</span><span class="sxs-lookup"><span data-stu-id="bf6ec-110">The number of samples of calling `op` to collect.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="bf6ec-111">entrada: ' TInput</span><span class="sxs-lookup"><span data-stu-id="bf6ec-111">input : 'TInput</span></span>

<span data-ttu-id="bf6ec-112">A entrada a ser passada para `op` .</span><span class="sxs-lookup"><span data-stu-id="bf6ec-112">The input to be passed to `op`.</span></span>



## <a name="output--toutput"></a><span data-ttu-id="bf6ec-113">Saída: ' TOutput []</span><span class="sxs-lookup"><span data-stu-id="bf6ec-113">Output : 'TOutput[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="bf6ec-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="bf6ec-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="bf6ec-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="bf6ec-115">'TInput</span></span>


### <a name="toutput"></a><span data-ttu-id="bf6ec-116">'TOutput</span><span class="sxs-lookup"><span data-stu-id="bf6ec-116">'TOutput</span></span>



## <a name="see-also"></a><span data-ttu-id="bf6ec-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="bf6ec-117">See Also</span></span>

- [<span data-ttu-id="bf6ec-118">Microsoft. Quantum. Canon. Repeat</span><span class="sxs-lookup"><span data-stu-id="bf6ec-118">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)