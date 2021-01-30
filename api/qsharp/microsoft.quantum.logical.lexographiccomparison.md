---
uid: Microsoft.Quantum.Logical.LexographicComparison
title: Função LexographicComparison
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LexographicComparison
qsharp.summary: Given a comparison function, returns a new function that lexographically compares two arrays.
ms.openlocfilehash: de8179ab6e835d08e7f41287f31a876b7ecc91c5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98814393"
---
# <a name="lexographiccomparison-function"></a><span data-ttu-id="a9c60-102">Função LexographicComparison</span><span class="sxs-lookup"><span data-stu-id="a9c60-102">LexographicComparison function</span></span>

<span data-ttu-id="a9c60-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="a9c60-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="a9c60-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a9c60-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a9c60-105">Dada uma função de comparação, retorna uma nova função que lexographically compara duas matrizes.</span><span class="sxs-lookup"><span data-stu-id="a9c60-105">Given a comparison function, returns a new function that lexographically compares two arrays.</span></span>

```qsharp
function LexographicComparison<'T> (elementComparison : (('T, 'T) -> Bool)) : (('T[], 'T[]) -> Bool)
```


## <a name="input"></a><span data-ttu-id="a9c60-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="a9c60-106">Input</span></span>

### <a name="elementcomparison--tt---bool"></a><span data-ttu-id="a9c60-107">elementComparison: (não, não)-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a9c60-107">elementComparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a9c60-108">Uma função que compara dois elementos `x` e `y` retorna se `x` é menor ou igual a `y` .</span><span class="sxs-lookup"><span data-stu-id="a9c60-108">A function that compares two elements `x` and `y` and returns if `x` is less than or equal to `y`.</span></span>



## <a name="output--tt---bool"></a><span data-ttu-id="a9c60-109">Saída: (t [], t [])-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a9c60-109">Output : ('T[],'T[]) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a9c60-110">Uma função que compara duas matrizes `xs` e `ys` retorna se `xs` ocorre antes ou igual a `ys` na ordenação de lexographical.</span><span class="sxs-lookup"><span data-stu-id="a9c60-110">A function that compares two arrays `xs` and `ys` and returns if `xs` occurs before or equal to `ys` in lexographical ordering.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a9c60-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="a9c60-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a9c60-112">T'</span><span class="sxs-lookup"><span data-stu-id="a9c60-112">'T</span></span>

<span data-ttu-id="a9c60-113">O tipo dos elementos das matrizes que estão sendo comparados.</span><span class="sxs-lookup"><span data-stu-id="a9c60-113">The type of the elements of the arrays being compared.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9c60-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9c60-114">Remarks</span></span>

<span data-ttu-id="a9c60-115">A comparação de lexographic entre duas matrizes `xs` e `ys` é definida pelo procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="a9c60-115">The lexographic comparison between two arrays `xs` and `ys` is defined by the following procedure.</span></span> <span data-ttu-id="a9c60-116">Dizemos que dois elementos `x` e `y` são equivalentes se `elementComparison(x, y)` e `elementComparison(y, x)` são ambos verdadeiros.</span><span class="sxs-lookup"><span data-stu-id="a9c60-116">We say that two elements `x` and `y` are equivalent if `elementComparison(x, y)` and `elementComparison(y, x)` are both true.</span></span>

- <span data-ttu-id="a9c60-117">Ambas as matrizes são comparadas elemento por elemento até o primeiro par de elementos que não são equivalentes.</span><span class="sxs-lookup"><span data-stu-id="a9c60-117">Both arrays are compared element-by-element until the first pair of elements that are not equivalent.</span></span> <span data-ttu-id="a9c60-118">A matriz que contém o elemento que ocorre primeiro de acordo com o `elementComparison` é mencionada primeiro na ordenação lexographical.</span><span class="sxs-lookup"><span data-stu-id="a9c60-118">The array containing the element that occurs first according to `elementComparison` is said to occur first in lexographical ordering.</span></span>
- <span data-ttu-id="a9c60-119">Se nenhum elemento inequivalente for encontrado e uma matriz for maior do que a outra, a matriz mais curta será mencionada primeiro.</span><span class="sxs-lookup"><span data-stu-id="a9c60-119">If no inequivalent elements are found, and one array is longer than the other, the shorter array is said to occur first.</span></span>

## <a name="see-also"></a><span data-ttu-id="a9c60-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="a9c60-120">See Also</span></span>

- [<span data-ttu-id="a9c60-121">Microsoft. Quantum. arrays. Classificed</span><span class="sxs-lookup"><span data-stu-id="a9c60-121">Microsoft.Quantum.Arrays.Sorted</span></span>](xref:Microsoft.Quantum.Arrays.Sorted)