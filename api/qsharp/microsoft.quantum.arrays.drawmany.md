---
uid: Microsoft.Quantum.Arrays.DrawMany
title: Operação DrawMany
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: DrawMany
qsharp.summary: Repeats an operation for a given number of samples, collecting its outputs in an array.
ms.openlocfilehash: bf63ce308679cef97c776d3383ff732ed4d4e500
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846214"
---
# <a name="drawmany-operation"></a><span data-ttu-id="246b4-102">Operação DrawMany</span><span class="sxs-lookup"><span data-stu-id="246b4-102">DrawMany operation</span></span>

<span data-ttu-id="246b4-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="246b4-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="246b4-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="246b4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="246b4-105">Repete uma operação para um determinado número de amostras, coletando suas saídas em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="246b4-105">Repeats an operation for a given number of samples, collecting its outputs in an array.</span></span>

```qsharp
operation DrawMany<'TInput, 'TOutput> (op : ('TInput => 'TOutput), nSamples : Int, input : 'TInput) : 'TOutput[]
```


## <a name="input"></a><span data-ttu-id="246b4-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="246b4-106">Input</span></span>

### <a name="op--tinput--toutput"></a><span data-ttu-id="246b4-107">op: ' TInput => ' TOutput</span><span class="sxs-lookup"><span data-stu-id="246b4-107">op : 'TInput => 'TOutput</span></span> 

<span data-ttu-id="246b4-108">A operação a ser chamada repetidamente.</span><span class="sxs-lookup"><span data-stu-id="246b4-108">The operation to be called repeatedly.</span></span>


### <a name="nsamples--int"></a><span data-ttu-id="246b4-109">nSamples: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="246b4-109">nSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="246b4-110">O número de amostras de chamada `op` para Collect.</span><span class="sxs-lookup"><span data-stu-id="246b4-110">The number of samples of calling `op` to collect.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="246b4-111">entrada: ' TInput</span><span class="sxs-lookup"><span data-stu-id="246b4-111">input : 'TInput</span></span>

<span data-ttu-id="246b4-112">A entrada a ser passada para `op` .</span><span class="sxs-lookup"><span data-stu-id="246b4-112">The input to be passed to `op`.</span></span>



## <a name="output--toutput"></a><span data-ttu-id="246b4-113">Saída: ' TOutput []</span><span class="sxs-lookup"><span data-stu-id="246b4-113">Output : 'TOutput[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="246b4-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="246b4-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="246b4-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="246b4-115">'TInput</span></span>


### <a name="toutput"></a><span data-ttu-id="246b4-116">'TOutput</span><span class="sxs-lookup"><span data-stu-id="246b4-116">'TOutput</span></span>



## <a name="example"></a><span data-ttu-id="246b4-117">Exemplo</span><span class="sxs-lookup"><span data-stu-id="246b4-117">Example</span></span>

<span data-ttu-id="246b4-118">O exemplo a seguir fornece um inteiro, dada uma operação que obtém um único bit por vez.</span><span class="sxs-lookup"><span data-stu-id="246b4-118">The following samples an integer, given an operation that samples a single bit at a time.</span></span>

```qsharp
let randomInteger = BoolArrayAsInt(DrawMany(SampleRandomBit, 16, ()));
```

## <a name="see-also"></a><span data-ttu-id="246b4-119">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="246b4-119">See Also</span></span>

- [<span data-ttu-id="246b4-120">Microsoft. Quantum. Canon. Repeat</span><span class="sxs-lookup"><span data-stu-id="246b4-120">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)