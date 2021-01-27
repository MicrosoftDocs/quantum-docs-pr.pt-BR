---
uid: Microsoft.Quantum.Arrays.Exclude
title: Função Exclude
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Exclude
qsharp.summary: Returns an array containing the elements of another array, excluding elements at a given list of indices.
ms.openlocfilehash: 76cdee56e84951c63e80babfdca6a3de33583cab
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848674"
---
# <a name="exclude-function"></a><span data-ttu-id="7b560-102">Função Exclude</span><span class="sxs-lookup"><span data-stu-id="7b560-102">Exclude function</span></span>

<span data-ttu-id="7b560-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="7b560-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="7b560-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7b560-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7b560-105">Retorna uma matriz que contém os elementos de outra matriz, excluindo os elementos em uma determinada lista de índices.</span><span class="sxs-lookup"><span data-stu-id="7b560-105">Returns an array containing the elements of another array, excluding elements at a given list of indices.</span></span>

```qsharp
function Exclude<'T> (remove : Int[], array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="7b560-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="7b560-106">Input</span></span>

### <a name="remove--int"></a><span data-ttu-id="7b560-107">remover: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="7b560-107">remove : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="7b560-108">Uma matriz de índices indicando quais elementos devem ser excluídos da saída.</span><span class="sxs-lookup"><span data-stu-id="7b560-108">An array of indices denoting which elements should be excluded from the output.</span></span>


### <a name="array--t"></a><span data-ttu-id="7b560-109">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="7b560-109">array : 'T[]</span></span>

<span data-ttu-id="7b560-110">Matriz da qual os valores na matriz de saída são obtidos.</span><span class="sxs-lookup"><span data-stu-id="7b560-110">Array of which the values in the output array are taken.</span></span>



## <a name="output--t"></a><span data-ttu-id="7b560-111">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="7b560-111">Output : 'T[]</span></span>

<span data-ttu-id="7b560-112">Uma matriz `output` que `output[0]` é o primeiro elemento de `array` cujo índice não aparece `remove` , tal como `output[1]` é o segundo elemento, e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="7b560-112">An array `output` such that `output[0]` is the first element of `array` whose index does not appear in `remove`, such that `output[1]` is the second such element, and so forth.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="7b560-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="7b560-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7b560-114">T'</span><span class="sxs-lookup"><span data-stu-id="7b560-114">'T</span></span>

<span data-ttu-id="7b560-115">O tipo dos elementos da matriz.</span><span class="sxs-lookup"><span data-stu-id="7b560-115">The type of the array elements.</span></span>

## <a name="example"></a><span data-ttu-id="7b560-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="7b560-116">Example</span></span>

```qsharp
let array = [10, 11, 12, 13, 14, 15];
// The following line returns [10, 12, 15].
let subarray = Exclude([1, 3, 4], array);
```