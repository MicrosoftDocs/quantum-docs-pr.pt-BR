---
uid: Microsoft.Quantum.Arrays.SequenceI
title: Função sequencei
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceI
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: d5dc4377c696e14b505c63701c2f5ca0dadca672
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694414"
---
# <a name="sequencei-function"></a><span data-ttu-id="a0697-102">Função sequencei</span><span class="sxs-lookup"><span data-stu-id="a0697-102">SequenceI function</span></span>

<span data-ttu-id="a0697-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="a0697-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="a0697-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a0697-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a0697-105">Obter uma matriz de inteiros em um determinado intervalo.</span><span class="sxs-lookup"><span data-stu-id="a0697-105">Get an array of integers in a given interval.</span></span>

```qsharp
function SequenceI (from : Int, to : Int) : Int[]
```


## <a name="input"></a><span data-ttu-id="a0697-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="a0697-106">Input</span></span>

### <a name="from--int"></a><span data-ttu-id="a0697-107">de: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a0697-107">from : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a0697-108">Um índice inicial inclusivo do intervalo.</span><span class="sxs-lookup"><span data-stu-id="a0697-108">An inclusive start index of the interval.</span></span>


### <a name="to--int"></a><span data-ttu-id="a0697-109">para: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a0697-109">to : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a0697-110">Um índice final inclusivo do intervalo que não é menor que `from` .</span><span class="sxs-lookup"><span data-stu-id="a0697-110">An inclusive end index of the interval that is not smaller than `from`.</span></span>



## <a name="output--int"></a><span data-ttu-id="a0697-111">Saída: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="a0697-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="a0697-112">Uma matriz que contém a sequência de números `from` , `from + 1` ,..., `to` .</span><span class="sxs-lookup"><span data-stu-id="a0697-112">An array containing the sequence of numbers `from`, `from + 1`, ..., `to`.</span></span>