---
uid: Microsoft.Quantum.Arrays.Windows
title: Função do Windows
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Windows
qsharp.summary: Returns all consecutive subarrays of length `size`.
ms.openlocfilehash: 8f32a23aa4379744b84c3b8d9c8f565e61c3c64e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219882"
---
# <a name="windows-function"></a><span data-ttu-id="7cc57-102">Função do Windows</span><span class="sxs-lookup"><span data-stu-id="7cc57-102">Windows function</span></span>

<span data-ttu-id="7cc57-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="7cc57-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="7cc57-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7cc57-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7cc57-105">Retorna todas as submatrizes consecutivas de comprimento `size` .</span><span class="sxs-lookup"><span data-stu-id="7cc57-105">Returns all consecutive subarrays of length `size`.</span></span>

```qsharp
function Windows<'T> (size : Int, array : 'T[]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="7cc57-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="7cc57-106">Description</span></span>

<span data-ttu-id="7cc57-107">Essa função retorna todas as `n - size + 1` submatrizes de length `size` em ordem, em que `n` é o comprimento de `arr` .</span><span class="sxs-lookup"><span data-stu-id="7cc57-107">This function returns all `n - size + 1` subarrays of length `size` in order, where `n` is the length of `arr`.</span></span>
<span data-ttu-id="7cc57-108">As primeiras submatrizes são `arr[0..size - 1], arr[1..size], arr[2..size + 1]` até a última submatriz `arr[n - size..n - 1]` .</span><span class="sxs-lookup"><span data-stu-id="7cc57-108">The first subarrays are `arr[0..size - 1], arr[1..size], arr[2..size + 1]` until the last subarray `arr[n - size..n - 1]`.</span></span>

<span data-ttu-id="7cc57-109">Se `size <= 0` ou `size > n` , uma matriz vazia será retornada.</span><span class="sxs-lookup"><span data-stu-id="7cc57-109">If `size <= 0` or `size > n`, an empty array is returned.</span></span>

## <a name="input"></a><span data-ttu-id="7cc57-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="7cc57-110">Input</span></span>

### <a name="size--int"></a><span data-ttu-id="7cc57-111">Tamanho: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7cc57-111">size : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7cc57-112">Comprimento das submatrizes.</span><span class="sxs-lookup"><span data-stu-id="7cc57-112">Length of the subarrays.</span></span>


### <a name="array--t"></a><span data-ttu-id="7cc57-113">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="7cc57-113">array : 'T[]</span></span>

<span data-ttu-id="7cc57-114">Uma matriz de elementos.</span><span class="sxs-lookup"><span data-stu-id="7cc57-114">An array of elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="7cc57-115">Saída: ' T' [] []</span><span class="sxs-lookup"><span data-stu-id="7cc57-115">Output : 'T[][]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="7cc57-116">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="7cc57-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7cc57-117">T'</span><span class="sxs-lookup"><span data-stu-id="7cc57-117">'T</span></span>

<span data-ttu-id="7cc57-118">O tipo de `array` elementos.</span><span class="sxs-lookup"><span data-stu-id="7cc57-118">The type of `array` elements.</span></span>