---
uid: Microsoft.Quantum.Arrays.Chunks
title: Função de partes
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Chunks
qsharp.summary: Splits an array into multiple parts of equal length.
ms.openlocfilehash: fe10999d35ed05908fd59b9dad8b5c0c51233ae6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694509"
---
# <a name="chunks-function"></a><span data-ttu-id="4ca06-102">Função de partes</span><span class="sxs-lookup"><span data-stu-id="4ca06-102">Chunks function</span></span>

<span data-ttu-id="4ca06-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="4ca06-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="4ca06-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4ca06-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4ca06-105">Divide uma matriz em várias partes de comprimento igual.</span><span class="sxs-lookup"><span data-stu-id="4ca06-105">Splits an array into multiple parts of equal length.</span></span>

```qsharp
function Chunks<'T> (nElements : Int, arr : 'T[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="4ca06-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="4ca06-106">Input</span></span>

### <a name="nelements--int"></a><span data-ttu-id="4ca06-107">nElements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4ca06-107">nElements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4ca06-108">O comprimento de cada parte.</span><span class="sxs-lookup"><span data-stu-id="4ca06-108">The length of each chunk.</span></span>


### <a name="arr--t"></a><span data-ttu-id="4ca06-109">arr: ' t []</span><span class="sxs-lookup"><span data-stu-id="4ca06-109">arr : 'T[]</span></span>

<span data-ttu-id="4ca06-110">A matriz a ser dividida.</span><span class="sxs-lookup"><span data-stu-id="4ca06-110">The array to be split.</span></span>



## <a name="output--t"></a><span data-ttu-id="4ca06-111">Saída: ' T' [] []</span><span class="sxs-lookup"><span data-stu-id="4ca06-111">Output : 'T[][]</span></span>

<span data-ttu-id="4ca06-112">Uma matriz que contém cada parte da matriz original.</span><span class="sxs-lookup"><span data-stu-id="4ca06-112">A array containing each chunk of the original array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="4ca06-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="4ca06-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4ca06-114">T'</span><span class="sxs-lookup"><span data-stu-id="4ca06-114">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="4ca06-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ca06-115">Remarks</span></span>

<span data-ttu-id="4ca06-116">Observe que o último elemento da saída pode ser menor do que `nElements` se `Length(arr)` não for divisível pelo `nElements` .</span><span class="sxs-lookup"><span data-stu-id="4ca06-116">Note that the last element of the output may be shorter than `nElements` if `Length(arr)` is not divisible by `nElements`.</span></span>