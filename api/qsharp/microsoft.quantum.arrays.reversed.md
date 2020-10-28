---
uid: Microsoft.Quantum.Arrays.Reversed
title: Função invertida
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Reversed
qsharp.summary: Create an array that contains the same elements as an input array but in Reversed order.
ms.openlocfilehash: 99244195e581dc00db24b938f5aa1c541cd4433a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694416"
---
# <a name="reversed-function"></a><span data-ttu-id="0eb54-102">Função invertida</span><span class="sxs-lookup"><span data-stu-id="0eb54-102">Reversed function</span></span>

<span data-ttu-id="0eb54-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="0eb54-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="0eb54-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0eb54-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0eb54-105">Crie uma matriz que contenha os mesmos elementos de uma matriz de entrada, mas em ordem inversa.</span><span class="sxs-lookup"><span data-stu-id="0eb54-105">Create an array that contains the same elements as an input array but in Reversed order.</span></span>

```qsharp
function Reversed<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="0eb54-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="0eb54-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="0eb54-107">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="0eb54-107">array : 'T[]</span></span>

<span data-ttu-id="0eb54-108">Uma matriz cujos elementos devem ser copiados na ordem inversa.</span><span class="sxs-lookup"><span data-stu-id="0eb54-108">An array whose elements are to be copied in Reversed order.</span></span>



## <a name="output--t"></a><span data-ttu-id="0eb54-109">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="0eb54-109">Output : 'T[]</span></span>

<span data-ttu-id="0eb54-110">Uma matriz que contém os elementos `array[Length(array) - 1]` ..</span><span class="sxs-lookup"><span data-stu-id="0eb54-110">An array containing the elements `array[Length(array) - 1]` ..</span></span> <span data-ttu-id="0eb54-111">`array[0]`.</span><span class="sxs-lookup"><span data-stu-id="0eb54-111">`array[0]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="0eb54-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="0eb54-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0eb54-113">T'</span><span class="sxs-lookup"><span data-stu-id="0eb54-113">'T</span></span>

<span data-ttu-id="0eb54-114">O tipo dos elementos da matriz.</span><span class="sxs-lookup"><span data-stu-id="0eb54-114">The type of the array elements.</span></span>