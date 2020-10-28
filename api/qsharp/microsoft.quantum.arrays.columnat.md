---
uid: Microsoft.Quantum.Arrays.ColumnAt
title: Função ColumnAt
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAt
qsharp.summary: Extracts a column from a matrix.
ms.openlocfilehash: ad09ada1a2253a54e70dddd6dba8aa243d2cd5a6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694507"
---
# <a name="columnat-function"></a><span data-ttu-id="67282-102">Função ColumnAt</span><span class="sxs-lookup"><span data-stu-id="67282-102">ColumnAt function</span></span>

<span data-ttu-id="67282-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="67282-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="67282-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="67282-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="67282-105">Extrai uma coluna de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="67282-105">Extracts a column from a matrix.</span></span>

```qsharp
function ColumnAt<'T> (column : Int, matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="67282-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="67282-106">Description</span></span>

<span data-ttu-id="67282-107">Essa função extrai uma coluna em uma matriz em ordem de linha.</span><span class="sxs-lookup"><span data-stu-id="67282-107">This function extracts a column in a matrix in row-wise order.</span></span>
<span data-ttu-id="67282-108">Extrair uma linha corrsponds para acesso de elemento do primeiro índice e, portanto, não requer tratamento adicional.</span><span class="sxs-lookup"><span data-stu-id="67282-108">Extracting a row corrsponds to element access of the first index and therefore requires no further treatment.</span></span>

## <a name="input"></a><span data-ttu-id="67282-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="67282-109">Input</span></span>

### <a name="column--int"></a><span data-ttu-id="67282-110">coluna: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="67282-110">column : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="67282-111">Coluna da matriz</span><span class="sxs-lookup"><span data-stu-id="67282-111">Column of the matrix</span></span>


### <a name="matrix--t"></a><span data-ttu-id="67282-112">matriz: t [] []</span><span class="sxs-lookup"><span data-stu-id="67282-112">matrix : 'T[][]</span></span>

<span data-ttu-id="67282-113">matriz 2-dimensional em ordem de linha</span><span class="sxs-lookup"><span data-stu-id="67282-113">2-dimensional matrix in row-wise order</span></span>



## <a name="output--t"></a><span data-ttu-id="67282-114">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="67282-114">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="67282-115">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="67282-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="67282-116">T'</span><span class="sxs-lookup"><span data-stu-id="67282-116">'T</span></span>

<span data-ttu-id="67282-117">O tipo de cada elemento de `matrix` .</span><span class="sxs-lookup"><span data-stu-id="67282-117">The type of each element of `matrix`.</span></span>

## <a name="see-also"></a><span data-ttu-id="67282-118">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="67282-118">See Also</span></span>

- [<span data-ttu-id="67282-119">Microsoft. Quantum. arrays. transposed</span><span class="sxs-lookup"><span data-stu-id="67282-119">Microsoft.Quantum.Arrays.Transposed</span></span>](xref:Microsoft.Quantum.Arrays.Transposed)
- [<span data-ttu-id="67282-120">Microsoft. Quantum. arrays. diagonal</span><span class="sxs-lookup"><span data-stu-id="67282-120">Microsoft.Quantum.Arrays.Diagonal</span></span>](xref:Microsoft.Quantum.Arrays.Diagonal)