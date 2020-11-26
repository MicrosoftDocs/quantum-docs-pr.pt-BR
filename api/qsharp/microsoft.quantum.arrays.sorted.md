---
uid: Microsoft.Quantum.Arrays.Sorted
title: Função classificada
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Sorted
qsharp.summary: Given an array, returns the elements of that array sorted by a given comparison function.
ms.openlocfilehash: bd8b869e03c7f4687c456a944e07a811ae0d2ce2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220222"
---
# <a name="sorted-function"></a><span data-ttu-id="518f4-102">Função classificada</span><span class="sxs-lookup"><span data-stu-id="518f4-102">Sorted function</span></span>

<span data-ttu-id="518f4-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="518f4-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="518f4-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="518f4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="518f4-105">Dada uma matriz, retorna os elementos dessa matriz classificados por uma determinada função de comparação.</span><span class="sxs-lookup"><span data-stu-id="518f4-105">Given an array, returns the elements of that array sorted by a given comparison function.</span></span>

```qsharp
function Sorted<'T> (comparison : (('T, 'T) -> Bool), array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="518f4-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="518f4-106">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="518f4-107">comparação: (não, não)-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="518f4-107">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="518f4-108">Uma função que compara dois elementos, de modo que `a` é considerado menor ou igual a `b` se `comparison(a, b)` for `true` .</span><span class="sxs-lookup"><span data-stu-id="518f4-108">A function that compares two elements such that `a` is considered to be less than or equal to `b` if `comparison(a, b)` is `true`.</span></span>


### <a name="array--t"></a><span data-ttu-id="518f4-109">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="518f4-109">array : 'T[]</span></span>

<span data-ttu-id="518f4-110">A matriz a ser classificada.</span><span class="sxs-lookup"><span data-stu-id="518f4-110">The array to be sorted.</span></span>



## <a name="output--t"></a><span data-ttu-id="518f4-111">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="518f4-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="518f4-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="518f4-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="518f4-113">T'</span><span class="sxs-lookup"><span data-stu-id="518f4-113">'T</span></span>

<span data-ttu-id="518f4-114">O tipo de cada elemento de `array` .</span><span class="sxs-lookup"><span data-stu-id="518f4-114">The type of each element of `array`.</span></span>

## <a name="remarks"></a><span data-ttu-id="518f4-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="518f4-115">Remarks</span></span>

<span data-ttu-id="518f4-116">Presume- `comparison` se que a função seja transitiva, de modo que, se `comparison(a, b)` e `comparison(b, c)` , `comparison(a, c)` for assumido.</span><span class="sxs-lookup"><span data-stu-id="518f4-116">The function `comparison` is assumed to be transitive, such that if `comparison(a, b)` and `comparison(b, c)`, then `comparison(a, c)` is assumed.</span></span> <span data-ttu-id="518f4-117">Se essa propriedade não for mantida, a saída dessa função poderá estar incorreta.</span><span class="sxs-lookup"><span data-stu-id="518f4-117">If this property does not hold, then the output of this function may be incorrect.</span></span>

<span data-ttu-id="518f4-118">Como se trata de uma função, os resultados são completamente determinísticass, mesmo quando dois elementos são considerados iguais em `comparison` ; ou seja, quando `comparison(a, b)` e `comparison(b, a)` são ambos `true` .</span><span class="sxs-lookup"><span data-stu-id="518f4-118">As this is a function, the results are completely determinstic, even when two elements are considered equal under `comparison`; that is, when `comparison(a, b)` and `comparison(b, a)` are both `true`.</span></span>
<span data-ttu-id="518f4-119">Em particular, a classificação executada por essa função é garantida como estável, de modo que, se dois elementos `a` e `b` ocorrer nessa ordem dentro `array` e sejam considerados iguais em `comparison` , `a` também aparecerão antes `b` na saída.</span><span class="sxs-lookup"><span data-stu-id="518f4-119">In particular, the sort performed by this function is guaranteed to be stable, so that if two elements `a` and `b` occur in that order within `array` and are considered equal under `comparison`, then `a` will also appear before `b` in the output.</span></span>

<span data-ttu-id="518f4-120">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="518f4-120">For example:</span></span>

```Q#
function LastDigitLessThanOrEqual(left : Int, right : Int) : Bool {
    return LessThanOrEqualI(
        left % 10, right % 10
    );
}

function SortedByLastDigit() : Int[] {
    return Sorted(LastDigitLessThanOrEqual, [3, 37, 11, 17]);
}
// returns [11, 3, 37, 17].
```