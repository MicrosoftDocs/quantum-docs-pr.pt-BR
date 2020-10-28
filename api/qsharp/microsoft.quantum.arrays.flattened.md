---
uid: Microsoft.Quantum.Arrays.Flattened
title: Função achatada
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Flattened
qsharp.summary: Given an array of arrays, returns the concatenation of all arrays.
ms.openlocfilehash: 91a35f0ac2c2f8609bac07734265fcf4e88bf50b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694471"
---
# <a name="flattened-function"></a><span data-ttu-id="2ca04-102">Função achatada</span><span class="sxs-lookup"><span data-stu-id="2ca04-102">Flattened function</span></span>

<span data-ttu-id="2ca04-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="2ca04-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="2ca04-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2ca04-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2ca04-105">Dada uma matriz de matrizes, retorna a concatenação de todas as matrizes.</span><span class="sxs-lookup"><span data-stu-id="2ca04-105">Given an array of arrays, returns the concatenation of all arrays.</span></span>

```qsharp
function Flattened<'T> (arrays : 'T[][]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="2ca04-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="2ca04-106">Input</span></span>

### <a name="arrays--t"></a><span data-ttu-id="2ca04-107">matrizes: ' t [] []</span><span class="sxs-lookup"><span data-stu-id="2ca04-107">arrays : 'T[][]</span></span>

<span data-ttu-id="2ca04-108">Matriz de matrizes.</span><span class="sxs-lookup"><span data-stu-id="2ca04-108">Array of arrays.</span></span>



## <a name="output--t"></a><span data-ttu-id="2ca04-109">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="2ca04-109">Output : 'T[]</span></span>

<span data-ttu-id="2ca04-110">Concatenação de todas as matrizes.</span><span class="sxs-lookup"><span data-stu-id="2ca04-110">Concatenation of all arrays.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="2ca04-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="2ca04-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2ca04-112">T'</span><span class="sxs-lookup"><span data-stu-id="2ca04-112">'T</span></span>

<span data-ttu-id="2ca04-113">O tipo de `array` elementos.</span><span class="sxs-lookup"><span data-stu-id="2ca04-113">The type of `array` elements.</span></span>