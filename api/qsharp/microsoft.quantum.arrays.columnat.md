---
uid: Microsoft.Quantum.Arrays.ColumnAt
title: Função ColumnAt
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAt
qsharp.summary: Extracts a column from a matrix.
ms.openlocfilehash: 097b3fdd6fc1843ada27052fcf08ee80d894d25a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210090"
---
# <a name="columnat-function"></a><span data-ttu-id="6a814-102">Função ColumnAt</span><span class="sxs-lookup"><span data-stu-id="6a814-102">ColumnAt function</span></span>

<span data-ttu-id="6a814-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="6a814-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="6a814-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6a814-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6a814-105">Extrai uma coluna de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="6a814-105">Extracts a column from a matrix.</span></span>

```qsharp
function ColumnAt<'T> (column : Int, matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="6a814-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="6a814-106">Description</span></span>

<span data-ttu-id="6a814-107">Essa função extrai uma coluna em uma matriz em ordem de linha.</span><span class="sxs-lookup"><span data-stu-id="6a814-107">This function extracts a column in a matrix in row-wise order.</span></span>
<span data-ttu-id="6a814-108">Extrair uma linha corrsponds para acesso de elemento do primeiro índice e, portanto, não requer tratamento adicional.</span><span class="sxs-lookup"><span data-stu-id="6a814-108">Extracting a row corrsponds to element access of the first index and therefore requires no further treatment.</span></span>

## <a name="input"></a><span data-ttu-id="6a814-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="6a814-109">Input</span></span>

### <a name="column--int"></a><span data-ttu-id="6a814-110">coluna: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6a814-110">column : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6a814-111">Coluna da matriz</span><span class="sxs-lookup"><span data-stu-id="6a814-111">Column of the matrix</span></span>


### <a name="matrix--t"></a><span data-ttu-id="6a814-112">matriz: t [] []</span><span class="sxs-lookup"><span data-stu-id="6a814-112">matrix : 'T[][]</span></span>

<span data-ttu-id="6a814-113">matriz 2-dimensional em ordem de linha</span><span class="sxs-lookup"><span data-stu-id="6a814-113">2-dimensional matrix in row-wise order</span></span>



## <a name="output--t"></a><span data-ttu-id="6a814-114">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="6a814-114">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="6a814-115">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="6a814-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6a814-116">T'</span><span class="sxs-lookup"><span data-stu-id="6a814-116">'T</span></span>

<span data-ttu-id="6a814-117">O tipo de cada elemento de `matrix` .</span><span class="sxs-lookup"><span data-stu-id="6a814-117">The type of each element of `matrix`.</span></span>

## <a name="see-also"></a><span data-ttu-id="6a814-118">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="6a814-118">See Also</span></span>

- [<span data-ttu-id="6a814-119">Microsoft. Quantum. arrays. transposed</span><span class="sxs-lookup"><span data-stu-id="6a814-119">Microsoft.Quantum.Arrays.Transposed</span></span>](xref:Microsoft.Quantum.Arrays.Transposed)
- [<span data-ttu-id="6a814-120">Microsoft. Quantum. arrays. diagonal</span><span class="sxs-lookup"><span data-stu-id="6a814-120">Microsoft.Quantum.Arrays.Diagonal</span></span>](xref:Microsoft.Quantum.Arrays.Diagonal)