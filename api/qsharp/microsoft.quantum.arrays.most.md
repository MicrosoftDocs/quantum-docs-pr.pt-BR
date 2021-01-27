---
uid: Microsoft.Quantum.Arrays.Most
title: A maioria das funções
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Most
qsharp.summary: Creates an array that is equal to an input array except that the last array element is dropped.
ms.openlocfilehash: 2b212b38ec55f3798eb9397f03b842573173eb88
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845578"
---
# <a name="most-function"></a><span data-ttu-id="3475c-102">A maioria das funções</span><span class="sxs-lookup"><span data-stu-id="3475c-102">Most function</span></span>

<span data-ttu-id="3475c-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="3475c-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="3475c-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3475c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3475c-105">Cria uma matriz que é igual a uma matriz de entrada, exceto que o último elemento da matriz é Descartado.</span><span class="sxs-lookup"><span data-stu-id="3475c-105">Creates an array that is equal to an input array except that the last array element is dropped.</span></span>

```qsharp
function Most<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="3475c-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="3475c-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="3475c-107">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="3475c-107">array : 'T[]</span></span>

<span data-ttu-id="3475c-108">Uma matriz cujos primeiros aos últimos elementos são formar a matriz de saída.</span><span class="sxs-lookup"><span data-stu-id="3475c-108">An array whose first to second-to-last elements are to form the output array.</span></span>



## <a name="output--t"></a><span data-ttu-id="3475c-109">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="3475c-109">Output : 'T[]</span></span>

<span data-ttu-id="3475c-110">Uma matriz que contém os elementos `array[0..Length(array) - 2]` .</span><span class="sxs-lookup"><span data-stu-id="3475c-110">An array containing the elements `array[0..Length(array) - 2]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="3475c-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="3475c-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3475c-112">T'</span><span class="sxs-lookup"><span data-stu-id="3475c-112">'T</span></span>

<span data-ttu-id="3475c-113">O tipo dos elementos da matriz.</span><span class="sxs-lookup"><span data-stu-id="3475c-113">The type of the array elements.</span></span>