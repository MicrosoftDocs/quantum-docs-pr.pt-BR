---
uid: Microsoft.Quantum.Arrays.Chunks
title: Função de partes
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Chunks
qsharp.summary: Splits an array into multiple parts of equal length.
ms.openlocfilehash: b323fdab1b207c72a4f46d5ca4cb368ecf0df818
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221599"
---
# <a name="chunks-function"></a><span data-ttu-id="aba4f-102">Função de partes</span><span class="sxs-lookup"><span data-stu-id="aba4f-102">Chunks function</span></span>

<span data-ttu-id="aba4f-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="aba4f-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="aba4f-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="aba4f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="aba4f-105">Divide uma matriz em várias partes de comprimento igual.</span><span class="sxs-lookup"><span data-stu-id="aba4f-105">Splits an array into multiple parts of equal length.</span></span>

```qsharp
function Chunks<'T> (nElements : Int, arr : 'T[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="aba4f-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="aba4f-106">Input</span></span>

### <a name="nelements--int"></a><span data-ttu-id="aba4f-107">nElements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="aba4f-107">nElements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="aba4f-108">O comprimento de cada parte.</span><span class="sxs-lookup"><span data-stu-id="aba4f-108">The length of each chunk.</span></span>


### <a name="arr--t"></a><span data-ttu-id="aba4f-109">arr: ' t []</span><span class="sxs-lookup"><span data-stu-id="aba4f-109">arr : 'T[]</span></span>

<span data-ttu-id="aba4f-110">A matriz a ser dividida.</span><span class="sxs-lookup"><span data-stu-id="aba4f-110">The array to be split.</span></span>



## <a name="output--t"></a><span data-ttu-id="aba4f-111">Saída: ' T' [] []</span><span class="sxs-lookup"><span data-stu-id="aba4f-111">Output : 'T[][]</span></span>

<span data-ttu-id="aba4f-112">Uma matriz que contém cada parte da matriz original.</span><span class="sxs-lookup"><span data-stu-id="aba4f-112">A array containing each chunk of the original array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="aba4f-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="aba4f-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="aba4f-114">T'</span><span class="sxs-lookup"><span data-stu-id="aba4f-114">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="aba4f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="aba4f-115">Remarks</span></span>

<span data-ttu-id="aba4f-116">Observe que o último elemento da saída pode ser menor do que `nElements` se `Length(arr)` não for divisível pelo `nElements` .</span><span class="sxs-lookup"><span data-stu-id="aba4f-116">Note that the last element of the output may be shorter than `nElements` if `Length(arr)` is not divisible by `nElements`.</span></span>