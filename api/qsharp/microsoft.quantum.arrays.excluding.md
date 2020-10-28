---
uid: Microsoft.Quantum.Arrays.Excluding
title: Excluindo função
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Excluding
qsharp.summary: Returns an array containing the elements of another array, excluding elements at a given list of indices.
ms.openlocfilehash: 8848c6e89da50efb4f7550168f1757b25a214a24
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694477"
---
# <a name="excluding-function"></a><span data-ttu-id="d6ade-102">Excluindo função</span><span class="sxs-lookup"><span data-stu-id="d6ade-102">Excluding function</span></span>

<span data-ttu-id="d6ade-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="d6ade-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="d6ade-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d6ade-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d6ade-105">Retorna uma matriz que contém os elementos de outra matriz, excluindo os elementos em uma determinada lista de índices.</span><span class="sxs-lookup"><span data-stu-id="d6ade-105">Returns an array containing the elements of another array, excluding elements at a given list of indices.</span></span>

```qsharp
function Excluding<'T> (remove : Int[], array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="d6ade-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="d6ade-106">Input</span></span>

### <a name="remove--int"></a><span data-ttu-id="d6ade-107">remover: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="d6ade-107">remove : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="d6ade-108">Uma matriz de índices indicando quais elementos devem ser excluídos da saída.</span><span class="sxs-lookup"><span data-stu-id="d6ade-108">An array of indices denoting which elements should be excluded from the output.</span></span>


### <a name="array--t"></a><span data-ttu-id="d6ade-109">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="d6ade-109">array : 'T[]</span></span>

<span data-ttu-id="d6ade-110">Matriz da qual os valores na matriz de saída são obtidos.</span><span class="sxs-lookup"><span data-stu-id="d6ade-110">Array of which the values in the output array are taken.</span></span>



## <a name="output--t"></a><span data-ttu-id="d6ade-111">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="d6ade-111">Output : 'T[]</span></span>

<span data-ttu-id="d6ade-112">Uma matriz `output` que `output[0]` é o primeiro elemento de `array` cujo índice não aparece `remove` , tal como `output[1]` é o segundo elemento, e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="d6ade-112">An array `output` such that `output[0]` is the first element of `array` whose index does not appear in `remove`, such that `output[1]` is the second such element, and so forth.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d6ade-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="d6ade-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d6ade-114">T'</span><span class="sxs-lookup"><span data-stu-id="d6ade-114">'T</span></span>

<span data-ttu-id="d6ade-115">O tipo dos elementos da matriz.</span><span class="sxs-lookup"><span data-stu-id="d6ade-115">The type of the array elements.</span></span>