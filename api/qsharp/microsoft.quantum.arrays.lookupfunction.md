---
uid: Microsoft.Quantum.Arrays.LookupFunction
title: Função LookupFunction
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: LookupFunction
qsharp.summary: Given an array, returns a function which returns elements of that array.
ms.openlocfilehash: db20795719d11138cbdc5a38c0a19d0f247af059
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220766"
---
# <a name="lookupfunction-function"></a><span data-ttu-id="d7eb1-102">Função LookupFunction</span><span class="sxs-lookup"><span data-stu-id="d7eb1-102">LookupFunction function</span></span>

<span data-ttu-id="d7eb1-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="d7eb1-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="d7eb1-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d7eb1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d7eb1-105">Dada uma matriz, retorna uma função que retorna elementos dessa matriz.</span><span class="sxs-lookup"><span data-stu-id="d7eb1-105">Given an array, returns a function which returns elements of that array.</span></span>

```qsharp
function LookupFunction<'T> (array : 'T[]) : (Int -> 'T)
```


## <a name="input"></a><span data-ttu-id="d7eb1-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="d7eb1-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="d7eb1-107">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="d7eb1-107">array : 'T[]</span></span>

<span data-ttu-id="d7eb1-108">A matriz a ser representada como uma função de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d7eb1-108">The array to be represented as a lookup function.</span></span>



## <a name="output--int---t"></a><span data-ttu-id="d7eb1-109">Saída: [int](xref:microsoft.quantum.lang-ref.int) -> ' t</span><span class="sxs-lookup"><span data-stu-id="d7eb1-109">Output : [Int](xref:microsoft.quantum.lang-ref.int) -> 'T</span></span>

<span data-ttu-id="d7eb1-110">Uma função `f` como essa `f(idx) == f[idx]` .</span><span class="sxs-lookup"><span data-stu-id="d7eb1-110">A function `f` such that `f(idx) == f[idx]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d7eb1-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="d7eb1-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d7eb1-112">T'</span><span class="sxs-lookup"><span data-stu-id="d7eb1-112">'T</span></span>

<span data-ttu-id="d7eb1-113">O tipo dos elementos da matriz que está sendo representada como uma função de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d7eb1-113">The type of the elements of the array being represented as a lookup function.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7eb1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7eb1-114">Remarks</span></span>

<span data-ttu-id="d7eb1-115">Essa função é útil principalmente para interoperar com funções e operações que usam `Int -> 'T` funções como seus argumentos.</span><span class="sxs-lookup"><span data-stu-id="d7eb1-115">This function is mainly useful for interoperating with functions and operations that take `Int -> 'T` functions as their arguments.</span></span> <span data-ttu-id="d7eb1-116">Isso é comum, por exemplo, na biblioteca de representação do gerador, em que as funções são usadas para evitar a necessidade de registrar uma matriz inteira na memória.</span><span class="sxs-lookup"><span data-stu-id="d7eb1-116">This is common, for instance, in the generator representation library, where functions are used to avoid the need to record an entire array in memory.</span></span>