---
uid: Microsoft.Quantum.Random.DrawCategorical
title: Operação DrawCategorical
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawCategorical
qsharp.summary: Draws a random sample from a categorical distribution specified by a list of probablities.
ms.openlocfilehash: fdc5ae3a9341cb11e8fda129bdd030289b6c99c2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694645"
---
# <a name="drawcategorical-operation"></a><span data-ttu-id="86e8a-102">Operação DrawCategorical</span><span class="sxs-lookup"><span data-stu-id="86e8a-102">DrawCategorical operation</span></span>

<span data-ttu-id="86e8a-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="86e8a-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="86e8a-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="86e8a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="86e8a-105">Desenha um exemplo aleatório de uma distribuição categórica especificada por uma lista de probablities.</span><span class="sxs-lookup"><span data-stu-id="86e8a-105">Draws a random sample from a categorical distribution specified by a list of probablities.</span></span>

```qsharp
operation DrawCategorical (probs : Double[]) : Int
```


## <a name="description"></a><span data-ttu-id="86e8a-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="86e8a-106">Description</span></span>

<span data-ttu-id="86e8a-107">A probabilidade de selecionar um índice específico é proporcional ao valor do elemento de matriz nesse índice.</span><span class="sxs-lookup"><span data-stu-id="86e8a-107">The probability of selecting a specific index is proportional to the value of the array element at that index.</span></span>
<span data-ttu-id="86e8a-108">Os elementos de matriz que são iguais a zero são ignorados e seus índices nunca são retornados.</span><span class="sxs-lookup"><span data-stu-id="86e8a-108">Array elements that are equal to zero are ignored and their indices are never returned.</span></span> <span data-ttu-id="86e8a-109">Se qualquer elemento de matriz for menor que zero, ou se nenhum elemento de matriz for maior que zero, a operação falhará.</span><span class="sxs-lookup"><span data-stu-id="86e8a-109">If any array element is less than zero, or if no array element is greater than zero, then the operation fails.</span></span>

## <a name="input"></a><span data-ttu-id="86e8a-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="86e8a-110">Input</span></span>

### <a name="probs--double"></a><span data-ttu-id="86e8a-111">Probes: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="86e8a-111">probs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="86e8a-112">Uma matriz de números de ponto flutuante proporcional à probabilidade de selecionar cada índice.</span><span class="sxs-lookup"><span data-stu-id="86e8a-112">An array of floating-point numbers proportional to the probability of selecting each index.</span></span>



## <a name="output--int"></a><span data-ttu-id="86e8a-113">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="86e8a-113">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="86e8a-114">Um inteiro $i $ com probabilidade $ \Pr (i) = p_i/\ sum_i p_i $, em que $p _i $ é o elemento $i $ th de `probs` .</span><span class="sxs-lookup"><span data-stu-id="86e8a-114">An integer $i$ with probability $\Pr(i) = p_i / \sum_i p_i$, where $p_i$ is the $i$th element of `probs`.</span></span>

## <a name="see-also"></a><span data-ttu-id="86e8a-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="86e8a-115">See Also</span></span>

- [<span data-ttu-id="86e8a-116">Microsoft. Quantum. Random. CategoricalDistribution</span><span class="sxs-lookup"><span data-stu-id="86e8a-116">Microsoft.Quantum.Random.CategoricalDistribution</span></span>](xref:Microsoft.Quantum.Random.CategoricalDistribution)