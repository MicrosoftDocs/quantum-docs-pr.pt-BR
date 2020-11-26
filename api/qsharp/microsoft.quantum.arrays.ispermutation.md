---
uid: Microsoft.Quantum.Arrays.IsPermutation
title: Função ismutation
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsPermutation
qsharp.summary: Outputs true if and only if a given array represents a permutation.
ms.openlocfilehash: 144f683818b5d75de5b075328365d3e994de29d1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220919"
---
# <a name="ispermutation-function"></a><span data-ttu-id="bd8ed-102">Função ismutation</span><span class="sxs-lookup"><span data-stu-id="bd8ed-102">IsPermutation function</span></span>

<span data-ttu-id="bd8ed-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="bd8ed-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="bd8ed-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bd8ed-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bd8ed-105">Gera true se e somente se uma determinada matriz representar uma permutação.</span><span class="sxs-lookup"><span data-stu-id="bd8ed-105">Outputs true if and only if a given array represents a permutation.</span></span>

```qsharp
function IsPermutation (permuation : Int[]) : Bool
```


## <a name="description"></a><span data-ttu-id="bd8ed-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="bd8ed-106">Description</span></span>

<span data-ttu-id="bd8ed-107">Dada uma matriz `array` de comprimento `n` , retorna true se e somente se cada inteiro de `0` para `n - 1` aparecer exatamente uma vez em `array` , de modo que `array` possa ser interpretado como uma permutação nos `n` elementos.</span><span class="sxs-lookup"><span data-stu-id="bd8ed-107">Given an array `array` of length `n`, returns true if and only if each integer from `0` to `n - 1` appears exactly once in `array`, such that `array` can be interpreted as a permutation on `n` elements.</span></span>

## <a name="input"></a><span data-ttu-id="bd8ed-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="bd8ed-108">Input</span></span>

### <a name="permuation--int"></a><span data-ttu-id="bd8ed-109">permuation: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="bd8ed-109">permuation : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="bd8ed-110">Uma matriz que pode ou não representar uma permutação.</span><span class="sxs-lookup"><span data-stu-id="bd8ed-110">An array that may or may not represent a permutation.</span></span>



## <a name="output--bool"></a><span data-ttu-id="bd8ed-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="bd8ed-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>



## <a name="remarks"></a><span data-ttu-id="bd8ed-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd8ed-112">Remarks</span></span>

<span data-ttu-id="bd8ed-113">Uma matriz de comprimento zero é uma simples permuta.</span><span class="sxs-lookup"><span data-stu-id="bd8ed-113">An array of length zero is trivially a permutation.</span></span>