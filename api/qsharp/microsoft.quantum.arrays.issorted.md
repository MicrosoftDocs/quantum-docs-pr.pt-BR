---
uid: Microsoft.Quantum.Arrays.IsSorted
title: Função IsSorted
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsSorted
qsharp.summary: Given an array, returns whether that array is sorted as defined by a given comparison function.
ms.openlocfilehash: 330c1f789585f64cf255bc74f8a9c1ccf81b009e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694448"
---
# <a name="issorted-function"></a><span data-ttu-id="a2a50-102">Função IsSorted</span><span class="sxs-lookup"><span data-stu-id="a2a50-102">IsSorted function</span></span>

<span data-ttu-id="a2a50-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="a2a50-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="a2a50-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a2a50-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a2a50-105">Dada uma matriz, retorna se essa matriz é classificada conforme definido por uma determinada função de comparação.</span><span class="sxs-lookup"><span data-stu-id="a2a50-105">Given an array, returns whether that array is sorted as defined by a given comparison function.</span></span>

```qsharp
function IsSorted<'T> (comparison : (('T, 'T) -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="a2a50-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="a2a50-106">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="a2a50-107">comparação: (não, não)-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a2a50-107">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a2a50-108">Uma função que compara dois elementos, de modo que `a` é considerado menor ou igual a `b` se `comparison(a, b)` for `true` .</span><span class="sxs-lookup"><span data-stu-id="a2a50-108">A function that compares two elements such that `a` is considered to be less than or equal to `b` if `comparison(a, b)` is `true`.</span></span>


### <a name="array--t"></a><span data-ttu-id="a2a50-109">matriz: ' t []</span><span class="sxs-lookup"><span data-stu-id="a2a50-109">array : 'T[]</span></span>

<span data-ttu-id="a2a50-110">A matriz a ser verificada.</span><span class="sxs-lookup"><span data-stu-id="a2a50-110">The array to be checked.</span></span>



## <a name="output--bool"></a><span data-ttu-id="a2a50-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a2a50-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a2a50-112">`true` se e somente se for para cada par de `a` elementos `b` e `array` ocorrer nessa ordem, `comparison(a, b)` será `true` .</span><span class="sxs-lookup"><span data-stu-id="a2a50-112">`true` if and only if for each pair of elements `a` and `b` of `array` occuring in that order, `comparison(a, b)` is `true`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a2a50-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="a2a50-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a2a50-114">T'</span><span class="sxs-lookup"><span data-stu-id="a2a50-114">'T</span></span>

<span data-ttu-id="a2a50-115">O tipo de cada elemento de `array` .</span><span class="sxs-lookup"><span data-stu-id="a2a50-115">The type of each element of `array`.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2a50-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2a50-116">Remarks</span></span>

<span data-ttu-id="a2a50-117">Presume- `comparison` se que a função seja transitiva, de modo que, se `comparison(a, b)` e `comparison(b, c)` , `comparison(a, c)` for assumido.</span><span class="sxs-lookup"><span data-stu-id="a2a50-117">The function `comparison` is assumed to be transitive, such that if `comparison(a, b)` and `comparison(b, c)`, then `comparison(a, c)` is assumed.</span></span> <span data-ttu-id="a2a50-118">Se essa propriedade não for mantida, a saída dessa função poderá estar incorreta.</span><span class="sxs-lookup"><span data-stu-id="a2a50-118">If this property does not hold, then the output of this function may be incorrect.</span></span>