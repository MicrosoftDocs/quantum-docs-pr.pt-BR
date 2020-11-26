---
uid: Microsoft.Quantum.Arrays.MostAndTail
title: Função MostAndTail
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MostAndTail
qsharp.summary: Returns a tuple of all but one and the last element of the array.
ms.openlocfilehash: 392efb20e4aaba80a77664444bb415d8bc9b0930
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220562"
---
# <a name="mostandtail-function"></a><span data-ttu-id="1f112-102">Função MostAndTail</span><span class="sxs-lookup"><span data-stu-id="1f112-102">MostAndTail function</span></span>

<span data-ttu-id="1f112-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="1f112-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="1f112-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1f112-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1f112-105">Retorna uma tupla de todos, exceto um e o último elemento da matriz.</span><span class="sxs-lookup"><span data-stu-id="1f112-105">Returns a tuple of all but one and the last element of the array.</span></span>

```qsharp
function MostAndTail<'A> (array : 'A[]) : ('A[], 'A)
```


## <a name="input"></a><span data-ttu-id="1f112-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="1f112-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="1f112-107">matriz: ' A []</span><span class="sxs-lookup"><span data-stu-id="1f112-107">array : 'A[]</span></span>

<span data-ttu-id="1f112-108">Uma matriz com pelo menos um elemento.</span><span class="sxs-lookup"><span data-stu-id="1f112-108">An array with at least one element.</span></span>



## <a name="output--aa"></a><span data-ttu-id="1f112-109">Saída: (' A [], ' A)</span><span class="sxs-lookup"><span data-stu-id="1f112-109">Output : ('A[],'A)</span></span>

<span data-ttu-id="1f112-110">Uma tupla de todos, exceto um e o último elemento da matriz.</span><span class="sxs-lookup"><span data-stu-id="1f112-110">A tuple of all but one and the last element of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="1f112-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="1f112-111">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="1f112-112">' A</span><span class="sxs-lookup"><span data-stu-id="1f112-112">'A</span></span>

<span data-ttu-id="1f112-113">O tipo dos elementos da matriz.</span><span class="sxs-lookup"><span data-stu-id="1f112-113">The type of the array elements.</span></span>