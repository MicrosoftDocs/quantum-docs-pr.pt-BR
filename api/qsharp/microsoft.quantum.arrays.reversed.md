---
uid: Microsoft.Quantum.Arrays.Reversed
title: Função invertida
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Reversed
qsharp.summary: Create an array that contains the same elements as an input array but in Reversed order.
ms.openlocfilehash: 270f15c1d10b4397e258c750876095efc2b8e951
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220426"
---
# <a name="reversed-function"></a><span data-ttu-id="6c2d2-102">Função invertida</span><span class="sxs-lookup"><span data-stu-id="6c2d2-102">Reversed function</span></span>

<span data-ttu-id="6c2d2-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="6c2d2-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="6c2d2-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6c2d2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6c2d2-105">Crie uma matriz que contenha os mesmos elementos de uma matriz de entrada, mas em ordem inversa.</span><span class="sxs-lookup"><span data-stu-id="6c2d2-105">Create an array that contains the same elements as an input array but in Reversed order.</span></span>

```qsharp
function Reversed<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="6c2d2-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c2d2-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="6c2d2-107">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="6c2d2-107">array : 'T[]</span></span>

<span data-ttu-id="6c2d2-108">Uma matriz cujos elementos devem ser copiados na ordem inversa.</span><span class="sxs-lookup"><span data-stu-id="6c2d2-108">An array whose elements are to be copied in Reversed order.</span></span>



## <a name="output--t"></a><span data-ttu-id="6c2d2-109">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="6c2d2-109">Output : 'T[]</span></span>

<span data-ttu-id="6c2d2-110">Uma matriz que contém os elementos `array[Length(array) - 1]` ..</span><span class="sxs-lookup"><span data-stu-id="6c2d2-110">An array containing the elements `array[Length(array) - 1]` ..</span></span> <span data-ttu-id="6c2d2-111">`array[0]`.</span><span class="sxs-lookup"><span data-stu-id="6c2d2-111">`array[0]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="6c2d2-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="6c2d2-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6c2d2-113">T'</span><span class="sxs-lookup"><span data-stu-id="6c2d2-113">'T</span></span>

<span data-ttu-id="6c2d2-114">O tipo dos elementos da matriz.</span><span class="sxs-lookup"><span data-stu-id="6c2d2-114">The type of the array elements.</span></span>