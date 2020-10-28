---
uid: Microsoft.Quantum.Arrays.HeadAndRest
title: Função HeadAndRest
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: HeadAndRest
qsharp.summary: Returns a tuple of first and all remaining elements of the array.
ms.openlocfilehash: 9af4ba48a21d3cdf932b2f702051a70a6108db1b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694461"
---
# <a name="headandrest-function"></a><span data-ttu-id="f2c4a-102">Função HeadAndRest</span><span class="sxs-lookup"><span data-stu-id="f2c4a-102">HeadAndRest function</span></span>

<span data-ttu-id="f2c4a-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="f2c4a-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="f2c4a-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f2c4a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f2c4a-105">Retorna uma tupla de primeiro e todos os elementos restantes da matriz.</span><span class="sxs-lookup"><span data-stu-id="f2c4a-105">Returns a tuple of first and all remaining elements of the array.</span></span>

```qsharp
function HeadAndRest<'A> (array : 'A[]) : ('A, 'A[])
```


## <a name="input"></a><span data-ttu-id="f2c4a-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="f2c4a-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="f2c4a-107">matriz: ' A []</span><span class="sxs-lookup"><span data-stu-id="f2c4a-107">array : 'A[]</span></span>

<span data-ttu-id="f2c4a-108">Uma matriz com pelo menos um elemento.</span><span class="sxs-lookup"><span data-stu-id="f2c4a-108">An array with at least one element.</span></span>



## <a name="output--aa"></a><span data-ttu-id="f2c4a-109">Saída: (' A ', ' A [])</span><span class="sxs-lookup"><span data-stu-id="f2c4a-109">Output : ('A,'A[])</span></span>

<span data-ttu-id="f2c4a-110">Uma tupla de primeiro e todos os elementos restantes da matriz.</span><span class="sxs-lookup"><span data-stu-id="f2c4a-110">A tuple of first and all remaining elements of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="f2c4a-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="f2c4a-111">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="f2c4a-112">' A</span><span class="sxs-lookup"><span data-stu-id="f2c4a-112">'A</span></span>

<span data-ttu-id="f2c4a-113">O tipo dos elementos da matriz.</span><span class="sxs-lookup"><span data-stu-id="f2c4a-113">The type of the array elements.</span></span>