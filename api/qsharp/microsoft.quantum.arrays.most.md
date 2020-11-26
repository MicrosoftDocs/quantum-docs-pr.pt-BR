---
uid: Microsoft.Quantum.Arrays.Most
title: A maioria das funções
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Most
qsharp.summary: Creates an array that is equal to an input array except that the last array element is dropped.
ms.openlocfilehash: 81e66e0b64ae8dfc44d163b68370ccadd191c729
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220596"
---
# <a name="most-function"></a><span data-ttu-id="47b19-102">A maioria das funções</span><span class="sxs-lookup"><span data-stu-id="47b19-102">Most function</span></span>

<span data-ttu-id="47b19-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="47b19-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="47b19-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="47b19-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="47b19-105">Cria uma matriz que é igual a uma matriz de entrada, exceto que o último elemento da matriz é Descartado.</span><span class="sxs-lookup"><span data-stu-id="47b19-105">Creates an array that is equal to an input array except that the last array element is dropped.</span></span>

```qsharp
function Most<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="47b19-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="47b19-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="47b19-107">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="47b19-107">array : 'T[]</span></span>

<span data-ttu-id="47b19-108">Uma matriz cujos primeiros aos últimos elementos são formar a matriz de saída.</span><span class="sxs-lookup"><span data-stu-id="47b19-108">An array whose first to second-to-last elements are to form the output array.</span></span>



## <a name="output--t"></a><span data-ttu-id="47b19-109">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="47b19-109">Output : 'T[]</span></span>

<span data-ttu-id="47b19-110">Uma matriz que contém os elementos `array[0..Length(array) - 2]` .</span><span class="sxs-lookup"><span data-stu-id="47b19-110">An array containing the elements `array[0..Length(array) - 2]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="47b19-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="47b19-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="47b19-112">T'</span><span class="sxs-lookup"><span data-stu-id="47b19-112">'T</span></span>

<span data-ttu-id="47b19-113">O tipo dos elementos da matriz.</span><span class="sxs-lookup"><span data-stu-id="47b19-113">The type of the array elements.</span></span>