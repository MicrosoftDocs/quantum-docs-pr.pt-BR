---
uid: Microsoft.Quantum.Arrays.Rest
title: Função REST
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Rest
qsharp.summary: Creates an array that is equal to an input array except that the first array element is dropped.
ms.openlocfilehash: 4dd10b6e8839fd906ca9c2e36c89c626d5772149
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220376"
---
# <a name="rest-function"></a><span data-ttu-id="66538-102">Função REST</span><span class="sxs-lookup"><span data-stu-id="66538-102">Rest function</span></span>

<span data-ttu-id="66538-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="66538-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="66538-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="66538-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="66538-105">Cria uma matriz que é igual a uma matriz de entrada, exceto que o primeiro elemento da matriz é Descartado.</span><span class="sxs-lookup"><span data-stu-id="66538-105">Creates an array that is equal to an input array except that the first array element is dropped.</span></span>

```qsharp
function Rest<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="66538-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="66538-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="66538-107">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="66538-107">array : 'T[]</span></span>

<span data-ttu-id="66538-108">Uma matriz cujo segundo para o último elementos é formar a matriz de saída.</span><span class="sxs-lookup"><span data-stu-id="66538-108">An array whose second to last elements are to form the output array.</span></span>



## <a name="output--t"></a><span data-ttu-id="66538-109">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="66538-109">Output : 'T[]</span></span>

<span data-ttu-id="66538-110">Uma matriz que contém os elementos `array[1..Length(array) - 1]` .</span><span class="sxs-lookup"><span data-stu-id="66538-110">An array containing the elements `array[1..Length(array) - 1]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="66538-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="66538-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="66538-112">T'</span><span class="sxs-lookup"><span data-stu-id="66538-112">'T</span></span>

<span data-ttu-id="66538-113">O tipo dos elementos da matriz.</span><span class="sxs-lookup"><span data-stu-id="66538-113">The type of the array elements.</span></span>