---
uid: Microsoft.Quantum.Arrays.SequenceL
title: Função sequencel
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceL
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: 3e5c7f64825f09d82792d3e46fe3f53f5814510b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220256"
---
# <a name="sequencel-function"></a><span data-ttu-id="ea8e7-102">Função sequencel</span><span class="sxs-lookup"><span data-stu-id="ea8e7-102">SequenceL function</span></span>

<span data-ttu-id="ea8e7-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="ea8e7-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="ea8e7-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ea8e7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ea8e7-105">Obter uma matriz de inteiros em um determinado intervalo.</span><span class="sxs-lookup"><span data-stu-id="ea8e7-105">Get an array of integers in a given interval.</span></span>

```qsharp
function SequenceL (from : BigInt, to : BigInt) : BigInt[]
```


## <a name="input"></a><span data-ttu-id="ea8e7-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="ea8e7-106">Input</span></span>

### <a name="from--bigint"></a><span data-ttu-id="ea8e7-107">de: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="ea8e7-107">from : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="ea8e7-108">Um índice inicial inclusivo do intervalo.</span><span class="sxs-lookup"><span data-stu-id="ea8e7-108">An inclusive start index of the interval.</span></span>


### <a name="to--bigint"></a><span data-ttu-id="ea8e7-109">para: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="ea8e7-109">to : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="ea8e7-110">Um índice final inclusivo do intervalo que não é menor que `from` .</span><span class="sxs-lookup"><span data-stu-id="ea8e7-110">An inclusive end index of the interval that is not smaller than `from`.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="ea8e7-111">Saída: [bigint](xref:microsoft.quantum.lang-ref.bigint)[]</span><span class="sxs-lookup"><span data-stu-id="ea8e7-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)[]</span></span>

<span data-ttu-id="ea8e7-112">Uma matriz que contém a sequência de números `from` , `from + 1` ,..., `to` .</span><span class="sxs-lookup"><span data-stu-id="ea8e7-112">An array containing the sequence of numbers `from`, `from + 1`, ..., `to`.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea8e7-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea8e7-113">Remarks</span></span>

<span data-ttu-id="ea8e7-114">A diferença entre `from` e `to` deve se ajustar a um `Int` valor.</span><span class="sxs-lookup"><span data-stu-id="ea8e7-114">The difference between `from` and `to` must fit into an `Int` value.</span></span>