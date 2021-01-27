---
uid: Microsoft.Quantum.Random.DrawCategorical
title: Operação DrawCategorical
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawCategorical
qsharp.summary: Draws a random sample from a categorical distribution specified by a list of probablities.
ms.openlocfilehash: a9fe1b08e80abc65a5c4b803f0cb8a5e7a62759c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851163"
---
# <a name="drawcategorical-operation"></a><span data-ttu-id="4ffeb-102">Operação DrawCategorical</span><span class="sxs-lookup"><span data-stu-id="4ffeb-102">DrawCategorical operation</span></span>

<span data-ttu-id="4ffeb-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="4ffeb-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="4ffeb-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="4ffeb-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="4ffeb-105">Desenha um exemplo aleatório de uma distribuição categórica especificada por uma lista de probablities.</span><span class="sxs-lookup"><span data-stu-id="4ffeb-105">Draws a random sample from a categorical distribution specified by a list of probablities.</span></span>

```qsharp
operation DrawCategorical (probs : Double[]) : Int
```


## <a name="description"></a><span data-ttu-id="4ffeb-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="4ffeb-106">Description</span></span>

<span data-ttu-id="4ffeb-107">A probabilidade de selecionar um índice específico é proporcional ao valor do elemento de matriz nesse índice.</span><span class="sxs-lookup"><span data-stu-id="4ffeb-107">The probability of selecting a specific index is proportional to the value of the array element at that index.</span></span>
<span data-ttu-id="4ffeb-108">Os elementos de matriz que são iguais a zero são ignorados e seus índices nunca são retornados.</span><span class="sxs-lookup"><span data-stu-id="4ffeb-108">Array elements that are equal to zero are ignored and their indices are never returned.</span></span> <span data-ttu-id="4ffeb-109">Se qualquer elemento de matriz for menor que zero, ou se nenhum elemento de matriz for maior que zero, a operação falhará.</span><span class="sxs-lookup"><span data-stu-id="4ffeb-109">If any array element is less than zero, or if no array element is greater than zero, then the operation fails.</span></span>

## <a name="input"></a><span data-ttu-id="4ffeb-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="4ffeb-110">Input</span></span>

### <a name="probs--double"></a><span data-ttu-id="4ffeb-111">Probes: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="4ffeb-111">probs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="4ffeb-112">Uma matriz de números de ponto flutuante proporcional à probabilidade de selecionar cada índice.</span><span class="sxs-lookup"><span data-stu-id="4ffeb-112">An array of floating-point numbers proportional to the probability of selecting each index.</span></span>



## <a name="output--int"></a><span data-ttu-id="4ffeb-113">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4ffeb-113">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4ffeb-114">Um inteiro $i $ com probabilidade $ \Pr (i) = p_i/\ sum_i p_i $, em que $p _i $ é o elemento $i $ th de `probs` .</span><span class="sxs-lookup"><span data-stu-id="4ffeb-114">An integer $i$ with probability $\Pr(i) = p_i / \sum_i p_i$, where $p_i$ is the $i$th element of `probs`.</span></span>

## <a name="see-also"></a><span data-ttu-id="4ffeb-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="4ffeb-115">See Also</span></span>

- [<span data-ttu-id="4ffeb-116">Microsoft. Quantum. Random. CategoricalDistribution</span><span class="sxs-lookup"><span data-stu-id="4ffeb-116">Microsoft.Quantum.Random.CategoricalDistribution</span></span>](xref:Microsoft.Quantum.Random.CategoricalDistribution)