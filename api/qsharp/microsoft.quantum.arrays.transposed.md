---
uid: Microsoft.Quantum.Arrays.Transposed
title: Função transpoda
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Transposed
qsharp.summary: Returns the transpose of a matrix represented as an array of arrays.
ms.openlocfilehash: f293399d8e3a2cb32b2929e8d1591ac5eaefd277
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219984"
---
# <a name="transposed-function"></a><span data-ttu-id="496cd-102">Função transpoda</span><span class="sxs-lookup"><span data-stu-id="496cd-102">Transposed function</span></span>

<span data-ttu-id="496cd-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="496cd-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="496cd-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="496cd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="496cd-105">Retorna a transpoção de uma matriz representada como uma matriz de matrizes.</span><span class="sxs-lookup"><span data-stu-id="496cd-105">Returns the transpose of a matrix represented as an array of arrays.</span></span>

```qsharp
function Transposed<'T> (matrix : 'T[][]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="496cd-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="496cd-106">Description</span></span>

<span data-ttu-id="496cd-107">Entrada como um $r \times c $ Matrix com $r $ Rows e $c $ Columns.</span><span class="sxs-lookup"><span data-stu-id="496cd-107">Input as an $r \times c$ matrix with $r$ rows and $c$ columns.</span></span>  <span data-ttu-id="496cd-108">A matriz é baseada em linha, ou seja, `matrix[i][j]` acessa o elemento na linha $i $ e coluna $j $.</span><span class="sxs-lookup"><span data-stu-id="496cd-108">The matrix is row-based, i.e., `matrix[i][j]` accesses the element at row $i$ and column $j$.</span></span>

<span data-ttu-id="496cd-109">Essa função retorna o $c \times r $ Matrix que é a transpoção da matriz de entrada.</span><span class="sxs-lookup"><span data-stu-id="496cd-109">This function returns the $c \times r$ matrix that is the transpose of the input matrix.</span></span>

## <a name="input"></a><span data-ttu-id="496cd-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="496cd-110">Input</span></span>

### <a name="matrix--t"></a><span data-ttu-id="496cd-111">matriz: t [] []</span><span class="sxs-lookup"><span data-stu-id="496cd-111">matrix : 'T[][]</span></span>

<span data-ttu-id="496cd-112">\Times com base em linha $r c $ Matrix</span><span class="sxs-lookup"><span data-stu-id="496cd-112">Row-based $r \times c$ matrix</span></span>



## <a name="output--t"></a><span data-ttu-id="496cd-113">Saída: ' T' [] []</span><span class="sxs-lookup"><span data-stu-id="496cd-113">Output : 'T[][]</span></span>

<span data-ttu-id="496cd-114">\Times transposed $c r $ Matrix</span><span class="sxs-lookup"><span data-stu-id="496cd-114">Transposed $c \times r$ matrix</span></span>

## <a name="type-parameters"></a><span data-ttu-id="496cd-115">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="496cd-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="496cd-116">T'</span><span class="sxs-lookup"><span data-stu-id="496cd-116">'T</span></span>

<span data-ttu-id="496cd-117">O tipo de cada elemento de `matrix` .</span><span class="sxs-lookup"><span data-stu-id="496cd-117">The type of each element of `matrix`.</span></span>