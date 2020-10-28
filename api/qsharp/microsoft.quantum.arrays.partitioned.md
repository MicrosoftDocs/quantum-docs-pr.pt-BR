---
uid: Microsoft.Quantum.Arrays.Partitioned
title: Função particionada
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Partitioned
qsharp.summary: Splits an array into multiple parts.
ms.openlocfilehash: e3395afeda206e255a58175b57245f91c588d978
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694427"
---
# <a name="partitioned-function"></a><span data-ttu-id="301d4-102">Função particionada</span><span class="sxs-lookup"><span data-stu-id="301d4-102">Partitioned function</span></span>

<span data-ttu-id="301d4-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="301d4-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="301d4-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="301d4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="301d4-105">Divide uma matriz em várias partes.</span><span class="sxs-lookup"><span data-stu-id="301d4-105">Splits an array into multiple parts.</span></span>

```qsharp
function Partitioned<'T> (nElements : Int[], arr : 'T[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="301d4-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="301d4-106">Input</span></span>

### <a name="nelements--int"></a><span data-ttu-id="301d4-107">nElements: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="301d4-107">nElements : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="301d4-108">Número de elementos em cada parte da matriz</span><span class="sxs-lookup"><span data-stu-id="301d4-108">Number of elements in each part of array</span></span>


### <a name="arr--t"></a><span data-ttu-id="301d4-109">arr: ' t []</span><span class="sxs-lookup"><span data-stu-id="301d4-109">arr : 'T[]</span></span>

<span data-ttu-id="301d4-110">Matriz de entrada a ser dividida.</span><span class="sxs-lookup"><span data-stu-id="301d4-110">Input array to be split.</span></span>



## <a name="output--t"></a><span data-ttu-id="301d4-111">Saída: ' T' [] []</span><span class="sxs-lookup"><span data-stu-id="301d4-111">Output : 'T[][]</span></span>

<span data-ttu-id="301d4-112">Várias matrizes em que a primeira matriz é a primeira `nElements[0]` de `arr` e a segunda matriz é a próxima `nElements[1]` de `arr` etc. A última matriz conterá todos os elementos restantes.</span><span class="sxs-lookup"><span data-stu-id="301d4-112">Multiple arrays where the first array is the first `nElements[0]` of `arr` and the second array are the next `nElements[1]` of `arr` etc. The last array will contain all remaining elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="301d4-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="301d4-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="301d4-114">T'</span><span class="sxs-lookup"><span data-stu-id="301d4-114">'T</span></span>

