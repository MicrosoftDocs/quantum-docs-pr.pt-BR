---
uid: Microsoft.Quantum.Arrays.IsPermutation
title: Função ismutation
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsPermutation
qsharp.summary: Outputs true if and only if a given array represents a permutation.
ms.openlocfilehash: 361bb21bedc725c25a1f3dfc811e9cfda4cb45ff
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694449"
---
# <a name="ispermutation-function"></a><span data-ttu-id="1f72e-102">Função ismutation</span><span class="sxs-lookup"><span data-stu-id="1f72e-102">IsPermutation function</span></span>

<span data-ttu-id="1f72e-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="1f72e-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="1f72e-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1f72e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1f72e-105">Gera true se e somente se uma determinada matriz representar uma permutação.</span><span class="sxs-lookup"><span data-stu-id="1f72e-105">Outputs true if and only if a given array represents a permutation.</span></span>

```qsharp
function IsPermutation (permuation : Int[]) : Bool
```


## <a name="description"></a><span data-ttu-id="1f72e-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f72e-106">Description</span></span>

<span data-ttu-id="1f72e-107">Dada uma matriz `array` de comprimento `n` , retorna true se e somente se cada inteiro de `0` para `n - 1` aparecer exatamente uma vez em `array` , de modo que `array` possa ser interpretado como uma permutação nos `n` elementos.</span><span class="sxs-lookup"><span data-stu-id="1f72e-107">Given an array `array` of length `n`, returns true if and only if each integer from `0` to `n - 1` appears exactly once in `array`, such that `array` can be interpreted as a permutation on `n` elements.</span></span>

## <a name="input"></a><span data-ttu-id="1f72e-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="1f72e-108">Input</span></span>

### <a name="permuation--int"></a><span data-ttu-id="1f72e-109">permuation: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="1f72e-109">permuation : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="1f72e-110">Uma matriz que pode ou não representar uma permutação.</span><span class="sxs-lookup"><span data-stu-id="1f72e-110">An array that may or may not represent a permutation.</span></span>



## <a name="output--bool"></a><span data-ttu-id="1f72e-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="1f72e-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>



## <a name="remarks"></a><span data-ttu-id="1f72e-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f72e-112">Remarks</span></span>

<span data-ttu-id="1f72e-113">Uma matriz de comprimento zero é uma simples permuta.</span><span class="sxs-lookup"><span data-stu-id="1f72e-113">An array of length zero is trivially a permutation.</span></span>