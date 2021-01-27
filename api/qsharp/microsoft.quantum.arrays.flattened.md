---
uid: Microsoft.Quantum.Arrays.Flattened
title: Função achatada
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Flattened
qsharp.summary: Given an array of arrays, returns the concatenation of all arrays.
ms.openlocfilehash: 272533d4efd8598b21daa341c867c070a2083ce0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848629"
---
# <a name="flattened-function"></a><span data-ttu-id="ef615-102">Função achatada</span><span class="sxs-lookup"><span data-stu-id="ef615-102">Flattened function</span></span>

<span data-ttu-id="ef615-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="ef615-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="ef615-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ef615-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ef615-105">Dada uma matriz de matrizes, retorna a concatenação de todas as matrizes.</span><span class="sxs-lookup"><span data-stu-id="ef615-105">Given an array of arrays, returns the concatenation of all arrays.</span></span>

```qsharp
function Flattened<'T> (arrays : 'T[][]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="ef615-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="ef615-106">Input</span></span>

### <a name="arrays--t"></a><span data-ttu-id="ef615-107">matrizes: ' t [] []</span><span class="sxs-lookup"><span data-stu-id="ef615-107">arrays : 'T[][]</span></span>

<span data-ttu-id="ef615-108">Matriz de matrizes.</span><span class="sxs-lookup"><span data-stu-id="ef615-108">Array of arrays.</span></span>



## <a name="output--t"></a><span data-ttu-id="ef615-109">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="ef615-109">Output : 'T[]</span></span>

<span data-ttu-id="ef615-110">Concatenação de todas as matrizes.</span><span class="sxs-lookup"><span data-stu-id="ef615-110">Concatenation of all arrays.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ef615-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="ef615-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ef615-112">T'</span><span class="sxs-lookup"><span data-stu-id="ef615-112">'T</span></span>

<span data-ttu-id="ef615-113">O tipo de `array` elementos.</span><span class="sxs-lookup"><span data-stu-id="ef615-113">The type of `array` elements.</span></span>

## <a name="example"></a><span data-ttu-id="ef615-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ef615-114">Example</span></span>

```qsharp
let flattened = Flattened([[1, 2], [3], [4, 5, 6]]);
// flattened = [1, 2, 3, 4, 5, 6]
```