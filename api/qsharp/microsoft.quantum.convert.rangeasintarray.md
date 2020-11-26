---
uid: Microsoft.Quantum.Convert.RangeAsIntArray
title: Função RangeAsIntArray
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: RangeAsIntArray
qsharp.summary: Creates an array `arr` of integers enumerated by start..step..end.
ms.openlocfilehash: f756e42aef7dc600e1fc6943a02513ac791f2320
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214000"
---
# <a name="rangeasintarray-function"></a><span data-ttu-id="ea72b-102">Função RangeAsIntArray</span><span class="sxs-lookup"><span data-stu-id="ea72b-102">RangeAsIntArray function</span></span>

<span data-ttu-id="ea72b-103">Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="ea72b-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="ea72b-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ea72b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ea72b-105">Cria uma matriz `arr` de inteiros enumerados por início.. etapa.. completo.</span><span class="sxs-lookup"><span data-stu-id="ea72b-105">Creates an array `arr` of integers enumerated by start..step..end.</span></span>

```qsharp
function RangeAsIntArray (range : Range) : Int[]
```


## <a name="input"></a><span data-ttu-id="ea72b-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="ea72b-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="ea72b-107">intervalo: [intervalo](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="ea72b-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="ea72b-108">Um `Range` dos valores `start..step..end` a serem convertidos em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="ea72b-108">A `Range` of values `start..step..end` to be converted to an array.</span></span>



## <a name="output--int"></a><span data-ttu-id="ea72b-109">Saída: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="ea72b-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="ea72b-110">Uma nova matriz de inteiros correspondentes a valores iterados por `range` .</span><span class="sxs-lookup"><span data-stu-id="ea72b-110">A new array of integers corresponding to values iterated over by `range`.</span></span>