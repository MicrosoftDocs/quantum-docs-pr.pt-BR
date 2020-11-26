---
uid: Microsoft.Quantum.Arrays.Flattened
title: Função achatada
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Flattened
qsharp.summary: Given an array of arrays, returns the concatenation of all arrays.
ms.openlocfilehash: 331b1714109259b21982e99d030aa0662e3aaadb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221208"
---
# <a name="flattened-function"></a><span data-ttu-id="4cd7e-102">Função achatada</span><span class="sxs-lookup"><span data-stu-id="4cd7e-102">Flattened function</span></span>

<span data-ttu-id="4cd7e-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="4cd7e-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="4cd7e-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4cd7e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4cd7e-105">Dada uma matriz de matrizes, retorna a concatenação de todas as matrizes.</span><span class="sxs-lookup"><span data-stu-id="4cd7e-105">Given an array of arrays, returns the concatenation of all arrays.</span></span>

```qsharp
function Flattened<'T> (arrays : 'T[][]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="4cd7e-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="4cd7e-106">Input</span></span>

### <a name="arrays--t"></a><span data-ttu-id="4cd7e-107">matrizes: ' t [] []</span><span class="sxs-lookup"><span data-stu-id="4cd7e-107">arrays : 'T[][]</span></span>

<span data-ttu-id="4cd7e-108">Matriz de matrizes.</span><span class="sxs-lookup"><span data-stu-id="4cd7e-108">Array of arrays.</span></span>



## <a name="output--t"></a><span data-ttu-id="4cd7e-109">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="4cd7e-109">Output : 'T[]</span></span>

<span data-ttu-id="4cd7e-110">Concatenação de todas as matrizes.</span><span class="sxs-lookup"><span data-stu-id="4cd7e-110">Concatenation of all arrays.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="4cd7e-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="4cd7e-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4cd7e-112">T'</span><span class="sxs-lookup"><span data-stu-id="4cd7e-112">'T</span></span>

<span data-ttu-id="4cd7e-113">O tipo de `array` elementos.</span><span class="sxs-lookup"><span data-stu-id="4cd7e-113">The type of `array` elements.</span></span>