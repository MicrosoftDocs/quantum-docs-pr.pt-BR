---
uid: Microsoft.Quantum.Arrays.Sorted
title: Função classificada
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Sorted
qsharp.summary: Given an array, returns the elements of that array sorted by a given comparison function.
ms.openlocfilehash: cb8a1ef438d798c8201ed9f52677e253770df1d3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845439"
---
# <a name="sorted-function"></a><span data-ttu-id="89637-102">Função classificada</span><span class="sxs-lookup"><span data-stu-id="89637-102">Sorted function</span></span>

<span data-ttu-id="89637-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="89637-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="89637-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="89637-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="89637-105">Dada uma matriz, retorna os elementos dessa matriz classificados por uma determinada função de comparação.</span><span class="sxs-lookup"><span data-stu-id="89637-105">Given an array, returns the elements of that array sorted by a given comparison function.</span></span>

```qsharp
function Sorted<'T> (comparison : (('T, 'T) -> Bool), array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="89637-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="89637-106">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="89637-107">comparação: (não, não)-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="89637-107">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="89637-108">Uma função que compara dois elementos, de modo que `a` é considerado menor ou igual a `b` se `comparison(a, b)` for `true` .</span><span class="sxs-lookup"><span data-stu-id="89637-108">A function that compares two elements such that `a` is considered to be less than or equal to `b` if `comparison(a, b)` is `true`.</span></span>


### <a name="array--t"></a><span data-ttu-id="89637-109">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="89637-109">array : 'T[]</span></span>

<span data-ttu-id="89637-110">A matriz a ser classificada.</span><span class="sxs-lookup"><span data-stu-id="89637-110">The array to be sorted.</span></span>



## <a name="output--t"></a><span data-ttu-id="89637-111">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="89637-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="89637-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="89637-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="89637-113">T'</span><span class="sxs-lookup"><span data-stu-id="89637-113">'T</span></span>

<span data-ttu-id="89637-114">O tipo de cada elemento de `array` .</span><span class="sxs-lookup"><span data-stu-id="89637-114">The type of each element of `array`.</span></span>

## <a name="example"></a><span data-ttu-id="89637-115">Exemplo</span><span class="sxs-lookup"><span data-stu-id="89637-115">Example</span></span>

<span data-ttu-id="89637-116">O trecho a seguir classifica uma matriz de inteiros para ocorrer em ordem crescente:</span><span class="sxs-lookup"><span data-stu-id="89637-116">The following snippet sorts an array of integers to occur in ascending order:</span></span>

```qsharp
let sortedArray = Sorted(LessThanOrEqualI, [3, 17, 11, -201, -11]);
```

## <a name="remarks"></a><span data-ttu-id="89637-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="89637-117">Remarks</span></span>

<span data-ttu-id="89637-118">Presume- `comparison` se que a função seja transitiva, de modo que, se `comparison(a, b)` e `comparison(b, c)` , `comparison(a, c)` for assumido.</span><span class="sxs-lookup"><span data-stu-id="89637-118">The function `comparison` is assumed to be transitive, such that if `comparison(a, b)` and `comparison(b, c)`, then `comparison(a, c)` is assumed.</span></span> <span data-ttu-id="89637-119">Se essa propriedade não for mantida, a saída dessa função poderá estar incorreta.</span><span class="sxs-lookup"><span data-stu-id="89637-119">If this property does not hold, then the output of this function may be incorrect.</span></span>

<span data-ttu-id="89637-120">Como se trata de uma função, os resultados são completamente determinísticass, mesmo quando dois elementos são considerados iguais em `comparison` ; ou seja, quando `comparison(a, b)` e `comparison(b, a)` são ambos `true` .</span><span class="sxs-lookup"><span data-stu-id="89637-120">As this is a function, the results are completely determinstic, even when two elements are considered equal under `comparison`; that is, when `comparison(a, b)` and `comparison(b, a)` are both `true`.</span></span>
<span data-ttu-id="89637-121">Em particular, a classificação executada por essa função é garantida como estável, de modo que, se dois elementos `a` e `b` ocorrer nessa ordem dentro `array` e sejam considerados iguais em `comparison` , `a` também aparecerão antes `b` na saída.</span><span class="sxs-lookup"><span data-stu-id="89637-121">In particular, the sort performed by this function is guaranteed to be stable, so that if two elements `a` and `b` occur in that order within `array` and are considered equal under `comparison`, then `a` will also appear before `b` in the output.</span></span>

<span data-ttu-id="89637-122">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="89637-122">For example:</span></span>

```qsharp
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