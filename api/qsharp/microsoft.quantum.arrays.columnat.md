---
uid: Microsoft.Quantum.Arrays.ColumnAt
title: Função ColumnAt
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAt
qsharp.summary: Extracts a column from a matrix.
ms.openlocfilehash: 32dc814de9b04563c2798a768f121723a1a8252c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846265"
---
# <a name="columnat-function"></a><span data-ttu-id="3a3c0-102">Função ColumnAt</span><span class="sxs-lookup"><span data-stu-id="3a3c0-102">ColumnAt function</span></span>

<span data-ttu-id="3a3c0-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="3a3c0-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="3a3c0-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3a3c0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3a3c0-105">Extrai uma coluna de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="3a3c0-105">Extracts a column from a matrix.</span></span>

```qsharp
function ColumnAt<'T> (column : Int, matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="3a3c0-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="3a3c0-106">Description</span></span>

<span data-ttu-id="3a3c0-107">Essa função extrai uma coluna em uma matriz em ordem de linha.</span><span class="sxs-lookup"><span data-stu-id="3a3c0-107">This function extracts a column in a matrix in row-wise order.</span></span>
<span data-ttu-id="3a3c0-108">Extrair uma linha corrsponds para acesso de elemento do primeiro índice e, portanto, não requer tratamento adicional.</span><span class="sxs-lookup"><span data-stu-id="3a3c0-108">Extracting a row corrsponds to element access of the first index and therefore requires no further treatment.</span></span>

## <a name="input"></a><span data-ttu-id="3a3c0-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="3a3c0-109">Input</span></span>

### <a name="column--int"></a><span data-ttu-id="3a3c0-110">coluna: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3a3c0-110">column : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3a3c0-111">Coluna da matriz</span><span class="sxs-lookup"><span data-stu-id="3a3c0-111">Column of the matrix</span></span>


### <a name="matrix--t"></a><span data-ttu-id="3a3c0-112">matriz: t [] []</span><span class="sxs-lookup"><span data-stu-id="3a3c0-112">matrix : 'T[][]</span></span>

<span data-ttu-id="3a3c0-113">matriz 2-dimensional em ordem de linha</span><span class="sxs-lookup"><span data-stu-id="3a3c0-113">2-dimensional matrix in row-wise order</span></span>



## <a name="output--t"></a><span data-ttu-id="3a3c0-114">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="3a3c0-114">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="3a3c0-115">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="3a3c0-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3a3c0-116">T'</span><span class="sxs-lookup"><span data-stu-id="3a3c0-116">'T</span></span>

<span data-ttu-id="3a3c0-117">O tipo de cada elemento de `matrix` .</span><span class="sxs-lookup"><span data-stu-id="3a3c0-117">The type of each element of `matrix`.</span></span>

## <a name="example"></a><span data-ttu-id="3a3c0-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3a3c0-118">Example</span></span>

```qsharp
let matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]];
let column = ColumnAt(0, matrix);
// same as: column = [1, 4, 7]
```

## <a name="see-also"></a><span data-ttu-id="3a3c0-119">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="3a3c0-119">See Also</span></span>

- [<span data-ttu-id="3a3c0-120">Microsoft. Quantum. arrays. transposed</span><span class="sxs-lookup"><span data-stu-id="3a3c0-120">Microsoft.Quantum.Arrays.Transposed</span></span>](xref:Microsoft.Quantum.Arrays.Transposed)
- [<span data-ttu-id="3a3c0-121">Microsoft. Quantum. arrays. diagonal</span><span class="sxs-lookup"><span data-stu-id="3a3c0-121">Microsoft.Quantum.Arrays.Diagonal</span></span>](xref:Microsoft.Quantum.Arrays.Diagonal)