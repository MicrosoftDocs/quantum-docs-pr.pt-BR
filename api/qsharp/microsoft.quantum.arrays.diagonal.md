---
uid: Microsoft.Quantum.Arrays.Diagonal
title: Função diagonal
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Diagonal
qsharp.summary: Returns an array of diagonal elements of a 2-dimensional array
ms.openlocfilehash: fe6bac0acfa07b14620c7c35ae5e1cec2287d13d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221531"
---
# <a name="diagonal-function"></a><span data-ttu-id="4b7da-102">Função diagonal</span><span class="sxs-lookup"><span data-stu-id="4b7da-102">Diagonal function</span></span>

<span data-ttu-id="4b7da-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="4b7da-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="4b7da-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4b7da-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4b7da-105">Retorna uma matriz de elementos diagonais de uma matriz bidimensional</span><span class="sxs-lookup"><span data-stu-id="4b7da-105">Returns an array of diagonal elements of a 2-dimensional array</span></span>

```qsharp
function Diagonal<'T> (matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="4b7da-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="4b7da-106">Description</span></span>

<span data-ttu-id="4b7da-107">Se a matriz bidimensional não tiver uma forma quadrada, a diagonal sobre o mínimo sobre o número de linhas e colunas será retornada.</span><span class="sxs-lookup"><span data-stu-id="4b7da-107">If the 2-dimensional array has not a square shape, the diagonal over the minimum over the number of rows and columns will be returned.</span></span>

## <a name="input"></a><span data-ttu-id="4b7da-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="4b7da-108">Input</span></span>

### <a name="matrix--t"></a><span data-ttu-id="4b7da-109">matriz: t [] []</span><span class="sxs-lookup"><span data-stu-id="4b7da-109">matrix : 'T[][]</span></span>

<span data-ttu-id="4b7da-110">matriz 2-dimensional em ordem de linha</span><span class="sxs-lookup"><span data-stu-id="4b7da-110">2-dimensional matrix in row-wise order</span></span>



## <a name="output--t"></a><span data-ttu-id="4b7da-111">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="4b7da-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="4b7da-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="4b7da-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4b7da-113">T'</span><span class="sxs-lookup"><span data-stu-id="4b7da-113">'T</span></span>

<span data-ttu-id="4b7da-114">O tipo de cada elemento de `matrix` .</span><span class="sxs-lookup"><span data-stu-id="4b7da-114">The type of each element of `matrix`.</span></span>

## <a name="see-also"></a><span data-ttu-id="4b7da-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="4b7da-115">See Also</span></span>

- [<span data-ttu-id="4b7da-116">Microsoft. Quantum. arrays. transposed</span><span class="sxs-lookup"><span data-stu-id="4b7da-116">Microsoft.Quantum.Arrays.Transposed</span></span>](xref:Microsoft.Quantum.Arrays.Transposed)