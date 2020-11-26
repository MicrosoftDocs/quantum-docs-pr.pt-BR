---
uid: Microsoft.Quantum.Arrays.SequenceI
title: Função sequencei
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceI
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: 5f03e5f2baff8077c1fa3fb5f1f079528ef0e215
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220290"
---
# <a name="sequencei-function"></a><span data-ttu-id="2b55d-102">Função sequencei</span><span class="sxs-lookup"><span data-stu-id="2b55d-102">SequenceI function</span></span>

<span data-ttu-id="2b55d-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="2b55d-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="2b55d-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2b55d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2b55d-105">Obter uma matriz de inteiros em um determinado intervalo.</span><span class="sxs-lookup"><span data-stu-id="2b55d-105">Get an array of integers in a given interval.</span></span>

```qsharp
function SequenceI (from : Int, to : Int) : Int[]
```


## <a name="input"></a><span data-ttu-id="2b55d-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="2b55d-106">Input</span></span>

### <a name="from--int"></a><span data-ttu-id="2b55d-107">de: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2b55d-107">from : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2b55d-108">Um índice inicial inclusivo do intervalo.</span><span class="sxs-lookup"><span data-stu-id="2b55d-108">An inclusive start index of the interval.</span></span>


### <a name="to--int"></a><span data-ttu-id="2b55d-109">para: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2b55d-109">to : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2b55d-110">Um índice final inclusivo do intervalo que não é menor que `from` .</span><span class="sxs-lookup"><span data-stu-id="2b55d-110">An inclusive end index of the interval that is not smaller than `from`.</span></span>



## <a name="output--int"></a><span data-ttu-id="2b55d-111">Saída: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="2b55d-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="2b55d-112">Uma matriz que contém a sequência de números `from` , `from + 1` ,..., `to` .</span><span class="sxs-lookup"><span data-stu-id="2b55d-112">An array containing the sequence of numbers `from`, `from + 1`, ..., `to`.</span></span>