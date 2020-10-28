---
uid: Microsoft.Quantum.Arrays.Most
title: A maioria das funções
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Most
qsharp.summary: Creates an array that is equal to an input array except that the last array element is dropped.
ms.openlocfilehash: ca89041a4e70472e9bf7a63ffcacccb35aad527c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694431"
---
# <a name="most-function"></a><span data-ttu-id="8036b-102">A maioria das funções</span><span class="sxs-lookup"><span data-stu-id="8036b-102">Most function</span></span>

<span data-ttu-id="8036b-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="8036b-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="8036b-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8036b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8036b-105">Cria uma matriz que é igual a uma matriz de entrada, exceto que o último elemento da matriz é Descartado.</span><span class="sxs-lookup"><span data-stu-id="8036b-105">Creates an array that is equal to an input array except that the last array element is dropped.</span></span>

```qsharp
function Most<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="8036b-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="8036b-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="8036b-107">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="8036b-107">array : 'T[]</span></span>

<span data-ttu-id="8036b-108">Uma matriz cujos primeiros aos últimos elementos são formar a matriz de saída.</span><span class="sxs-lookup"><span data-stu-id="8036b-108">An array whose first to second-to-last elements are to form the output array.</span></span>



## <a name="output--t"></a><span data-ttu-id="8036b-109">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="8036b-109">Output : 'T[]</span></span>

<span data-ttu-id="8036b-110">Uma matriz que contém os elementos `array[0..Length(array) - 2]` .</span><span class="sxs-lookup"><span data-stu-id="8036b-110">An array containing the elements `array[0..Length(array) - 2]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="8036b-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="8036b-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8036b-112">T'</span><span class="sxs-lookup"><span data-stu-id="8036b-112">'T</span></span>

<span data-ttu-id="8036b-113">O tipo dos elementos da matriz.</span><span class="sxs-lookup"><span data-stu-id="8036b-113">The type of the array elements.</span></span>