---
uid: Microsoft.Quantum.Canon.RepeatCA
title: Operação RepeatCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatCA
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: af93220562d6be27b2f41e770bd953e5e808fcbf
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852203"
---
# <a name="repeatca-operation"></a><span data-ttu-id="31674-102">Operação RepeatCA</span><span class="sxs-lookup"><span data-stu-id="31674-102">RepeatCA operation</span></span>

<span data-ttu-id="31674-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="31674-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="31674-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="31674-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="31674-105">Repete uma operação um determinado número de vezes.</span><span class="sxs-lookup"><span data-stu-id="31674-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation RepeatCA<'TInput> (op : ('TInput => Unit is Adj + Ctl), nTimes : Int, input : 'TInput) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="31674-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="31674-106">Input</span></span>

### <a name="op--tinput--unit--is-adj--ctl"></a><span data-ttu-id="31674-107">op: a [unidade](xref:microsoft.quantum.lang-ref.unit)  ' TInput => é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="31674-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="31674-108">A operação a ser chamada repetidamente.</span><span class="sxs-lookup"><span data-stu-id="31674-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="31674-109">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="31674-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="31674-110">O número de vezes para chamar `op` .</span><span class="sxs-lookup"><span data-stu-id="31674-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="31674-111">entrada: ' TInput</span><span class="sxs-lookup"><span data-stu-id="31674-111">input : 'TInput</span></span>

<span data-ttu-id="31674-112">A entrada a ser passada para `op` .</span><span class="sxs-lookup"><span data-stu-id="31674-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="31674-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="31674-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="31674-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="31674-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="31674-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="31674-115">'TInput</span></span>



## <a name="example"></a><span data-ttu-id="31674-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="31674-116">Example</span></span>

<span data-ttu-id="31674-117">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="31674-117">The following are equivalent:</span></span>

```qsharp
RepeatCA(U, 17, target);
(BoundCA(ConstantArray(17, U)))(target);
```

## <a name="see-also"></a><span data-ttu-id="31674-118">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="31674-118">See Also</span></span>

- [<span data-ttu-id="31674-119">Microsoft. Quantum. arrays. DrawMany</span><span class="sxs-lookup"><span data-stu-id="31674-119">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="31674-120">Microsoft. Quantum. Canon. Repeat</span><span class="sxs-lookup"><span data-stu-id="31674-120">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)
- [<span data-ttu-id="31674-121">Microsoft. Quantum. Canon. REPEATA</span><span class="sxs-lookup"><span data-stu-id="31674-121">Microsoft.Quantum.Canon.RepeatA</span></span>](xref:Microsoft.Quantum.Canon.RepeatA)
- [<span data-ttu-id="31674-122">Microsoft. Quantum. Canon. RepeatC</span><span class="sxs-lookup"><span data-stu-id="31674-122">Microsoft.Quantum.Canon.RepeatC</span></span>](xref:Microsoft.Quantum.Canon.RepeatC)