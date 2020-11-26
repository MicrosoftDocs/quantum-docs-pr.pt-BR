---
uid: Microsoft.Quantum.Arrays.Partitioned
title: Função particionada
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Partitioned
qsharp.summary: Splits an array into multiple parts.
ms.openlocfilehash: bce46262e3ef64a43e578098d81c5dd39225915e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220494"
---
# <a name="partitioned-function"></a><span data-ttu-id="fc402-102">Função particionada</span><span class="sxs-lookup"><span data-stu-id="fc402-102">Partitioned function</span></span>

<span data-ttu-id="fc402-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="fc402-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="fc402-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fc402-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fc402-105">Divide uma matriz em várias partes.</span><span class="sxs-lookup"><span data-stu-id="fc402-105">Splits an array into multiple parts.</span></span>

```qsharp
function Partitioned<'T> (nElements : Int[], arr : 'T[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="fc402-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="fc402-106">Input</span></span>

### <a name="nelements--int"></a><span data-ttu-id="fc402-107">nElements: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="fc402-107">nElements : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="fc402-108">Número de elementos em cada parte da matriz</span><span class="sxs-lookup"><span data-stu-id="fc402-108">Number of elements in each part of array</span></span>


### <a name="arr--t"></a><span data-ttu-id="fc402-109">arr: ' t []</span><span class="sxs-lookup"><span data-stu-id="fc402-109">arr : 'T[]</span></span>

<span data-ttu-id="fc402-110">Matriz de entrada a ser dividida.</span><span class="sxs-lookup"><span data-stu-id="fc402-110">Input array to be split.</span></span>



## <a name="output--t"></a><span data-ttu-id="fc402-111">Saída: ' T' [] []</span><span class="sxs-lookup"><span data-stu-id="fc402-111">Output : 'T[][]</span></span>

<span data-ttu-id="fc402-112">Várias matrizes em que a primeira matriz é a primeira `nElements[0]` de `arr` e a segunda matriz é a próxima `nElements[1]` de `arr` etc. A última matriz conterá todos os elementos restantes.</span><span class="sxs-lookup"><span data-stu-id="fc402-112">Multiple arrays where the first array is the first `nElements[0]` of `arr` and the second array are the next `nElements[1]` of `arr` etc. The last array will contain all remaining elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="fc402-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="fc402-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="fc402-114">T'</span><span class="sxs-lookup"><span data-stu-id="fc402-114">'T</span></span>

