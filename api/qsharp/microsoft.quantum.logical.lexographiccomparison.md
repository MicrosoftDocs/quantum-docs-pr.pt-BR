---
uid: Microsoft.Quantum.Logical.LexographicComparison
title: Função LexographicComparison
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LexographicComparison
qsharp.summary: Given a comparison function, returns a new function that lexographically compares two arrays.
ms.openlocfilehash: f0b68974a0ea26907b58971e4fa4b1f06f5714d2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693113"
---
# <a name="lexographiccomparison-function"></a><span data-ttu-id="5ac66-102">Função LexographicComparison</span><span class="sxs-lookup"><span data-stu-id="5ac66-102">LexographicComparison function</span></span>

<span data-ttu-id="5ac66-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="5ac66-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="5ac66-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5ac66-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5ac66-105">Dada uma função de comparação, retorna uma nova função que lexographically compara duas matrizes.</span><span class="sxs-lookup"><span data-stu-id="5ac66-105">Given a comparison function, returns a new function that lexographically compares two arrays.</span></span>

```qsharp
function LexographicComparison<'T> (elementComparison : (('T, 'T) -> Bool)) : (('T[], 'T[]) -> Bool)
```


## <a name="input"></a><span data-ttu-id="5ac66-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="5ac66-106">Input</span></span>

### <a name="elementcomparison--tt---bool"></a><span data-ttu-id="5ac66-107">elementComparison: (não, não)-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="5ac66-107">elementComparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="5ac66-108">Uma função que compara dois elementos `x` e `y` retorna se `x` é menor ou igual a `y` .</span><span class="sxs-lookup"><span data-stu-id="5ac66-108">A function that compares two elements `x` and `y` and returns if `x` is less than or equal to `y`.</span></span>



## <a name="output--tt---bool"></a><span data-ttu-id="5ac66-109">Saída: (t [], t [])-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="5ac66-109">Output : ('T[],'T[]) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="5ac66-110">Uma função que compara duas matrizes `xs` e `ys` retorna se `xs` ocorre antes ou igual a `ys` na ordenação de lexographical.</span><span class="sxs-lookup"><span data-stu-id="5ac66-110">A function that compares two arrays `xs` and `ys` and returns if `xs` occurs before or equal to `ys` in lexographical ordering.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="5ac66-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="5ac66-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5ac66-112">T'</span><span class="sxs-lookup"><span data-stu-id="5ac66-112">'T</span></span>

<span data-ttu-id="5ac66-113">O tipo dos elementos das matrizes que estão sendo comparados.</span><span class="sxs-lookup"><span data-stu-id="5ac66-113">The type of the elements of the arrays being compared.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ac66-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5ac66-114">Remarks</span></span>

<span data-ttu-id="5ac66-115">A comparação de lexographic entre duas matrizes `xs` e `ys` é definida pelo procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="5ac66-115">The lexographic comparison between two arrays `xs` and `ys` is defined by the following procedure.</span></span> <span data-ttu-id="5ac66-116">Dizemos que dois elementos `x` e `y` são equivalentes se `elementComparison(x, y)` e `elementComparison(y, x)` são ambos verdadeiros.</span><span class="sxs-lookup"><span data-stu-id="5ac66-116">We say that two elements `x` and `y` are equivalent if `elementComparison(x, y)` and `elementComparison(y, x)` are both true.</span></span>

- <span data-ttu-id="5ac66-117">Ambas as matrizes são comparadas elemento por elemento até o primeiro par de elementos que não são equivalentes.</span><span class="sxs-lookup"><span data-stu-id="5ac66-117">Both arrays are compared element-by-element until the first pair of elements that are not equivalent.</span></span> <span data-ttu-id="5ac66-118">A matriz que contém o elemento que ocorre primeiro de acordo com o `elementComparison` é mencionada primeiro na ordenação lexographical.</span><span class="sxs-lookup"><span data-stu-id="5ac66-118">The array containing the element that occurs first according to `elementComparison` is said to occur first in lexographical ordering.</span></span>
- <span data-ttu-id="5ac66-119">Se nenhum elemento inequivalente for encontrado e uma matriz for maior do que a outra, a matriz mais curta será mencionada primeiro.</span><span class="sxs-lookup"><span data-stu-id="5ac66-119">If no inequivalent elements are found, and one array is longer than the other, the shorter array is said to occur first.</span></span>

## <a name="see-also"></a><span data-ttu-id="5ac66-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="5ac66-120">See Also</span></span>

- [<span data-ttu-id="5ac66-121">Microsoft. Quantum. arrays. Classificed</span><span class="sxs-lookup"><span data-stu-id="5ac66-121">Microsoft.Quantum.Arrays.Sorted</span></span>](xref:Microsoft.Quantum.Arrays.Sorted)