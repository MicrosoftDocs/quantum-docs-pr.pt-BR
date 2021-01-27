---
uid: Microsoft.Quantum.Arrays.Transposed
title: Função transpoda
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Transposed
qsharp.summary: Returns the transpose of a matrix represented as an array of arrays.
ms.openlocfilehash: 913f1829ef53ec3eb6944be8b8e3eb37b431f27e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850927"
---
# <a name="transposed-function"></a><span data-ttu-id="e77e2-102">Função transpoda</span><span class="sxs-lookup"><span data-stu-id="e77e2-102">Transposed function</span></span>

<span data-ttu-id="e77e2-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="e77e2-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="e77e2-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e77e2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e77e2-105">Retorna a transpoção de uma matriz representada como uma matriz de matrizes.</span><span class="sxs-lookup"><span data-stu-id="e77e2-105">Returns the transpose of a matrix represented as an array of arrays.</span></span>

```qsharp
function Transposed<'T> (matrix : 'T[][]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="e77e2-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="e77e2-106">Description</span></span>

<span data-ttu-id="e77e2-107">Entrada como um $r \times c $ Matrix com $r $ Rows e $c $ Columns.</span><span class="sxs-lookup"><span data-stu-id="e77e2-107">Input as an $r \times c$ matrix with $r$ rows and $c$ columns.</span></span>  <span data-ttu-id="e77e2-108">A matriz é baseada em linha, ou seja, `matrix[i][j]` acessa o elemento na linha $i $ e coluna $j $.</span><span class="sxs-lookup"><span data-stu-id="e77e2-108">The matrix is row-based, i.e., `matrix[i][j]` accesses the element at row $i$ and column $j$.</span></span>

<span data-ttu-id="e77e2-109">Essa função retorna o $c \times r $ Matrix que é a transpoção da matriz de entrada.</span><span class="sxs-lookup"><span data-stu-id="e77e2-109">This function returns the $c \times r$ matrix that is the transpose of the input matrix.</span></span>

## <a name="input"></a><span data-ttu-id="e77e2-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="e77e2-110">Input</span></span>

### <a name="matrix--t"></a><span data-ttu-id="e77e2-111">matriz: t [] []</span><span class="sxs-lookup"><span data-stu-id="e77e2-111">matrix : 'T[][]</span></span>

<span data-ttu-id="e77e2-112">\Times com base em linha $r c $ Matrix</span><span class="sxs-lookup"><span data-stu-id="e77e2-112">Row-based $r \times c$ matrix</span></span>



## <a name="output--t"></a><span data-ttu-id="e77e2-113">Saída: ' T' [] []</span><span class="sxs-lookup"><span data-stu-id="e77e2-113">Output : 'T[][]</span></span>

<span data-ttu-id="e77e2-114">\Times transposed $c r $ Matrix</span><span class="sxs-lookup"><span data-stu-id="e77e2-114">Transposed $c \times r$ matrix</span></span>

## <a name="type-parameters"></a><span data-ttu-id="e77e2-115">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="e77e2-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e77e2-116">T'</span><span class="sxs-lookup"><span data-stu-id="e77e2-116">'T</span></span>

<span data-ttu-id="e77e2-117">O tipo de cada elemento de `matrix` .</span><span class="sxs-lookup"><span data-stu-id="e77e2-117">The type of each element of `matrix`.</span></span>

## <a name="example"></a><span data-ttu-id="e77e2-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e77e2-118">Example</span></span>

```qsharp
// same as [[1, 4], [2, 5], [3, 6]]
let transposed = Transposed([[1, 2, 3], [4, 5, 6]]);
```