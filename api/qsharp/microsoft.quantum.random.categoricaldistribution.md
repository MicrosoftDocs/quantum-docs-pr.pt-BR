---
uid: Microsoft.Quantum.Random.CategoricalDistribution
title: Função CategoricalDistribution
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: CategoricalDistribution
qsharp.summary: Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.
ms.openlocfilehash: 756e9e95cac5554ab8f885dab7c47ac1b174c0f3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92695041"
---
# <a name="categoricaldistribution-function"></a><span data-ttu-id="12a1b-102">Função CategoricalDistribution</span><span class="sxs-lookup"><span data-stu-id="12a1b-102">CategoricalDistribution function</span></span>

<span data-ttu-id="12a1b-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="12a1b-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="12a1b-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="12a1b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="12a1b-105">Retorna uma distribuição categórica discreta, na qual a probabilidade de cada uma lista finita de resultados determinados é especificada explicitamente.</span><span class="sxs-lookup"><span data-stu-id="12a1b-105">Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.</span></span>

```qsharp
function CategoricalDistribution (probs : Double[]) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a><span data-ttu-id="12a1b-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="12a1b-106">Input</span></span>

### <a name="probs--double"></a><span data-ttu-id="12a1b-107">Probes: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="12a1b-107">probs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="12a1b-108">As probabilidades para cada resultado da distribuição categórica.</span><span class="sxs-lookup"><span data-stu-id="12a1b-108">The probabilities for each outcome from the categorical distribution.</span></span>
<span data-ttu-id="12a1b-109">Essas probabilidades não podem ser normalizadas, mas devem ser não negativas.</span><span class="sxs-lookup"><span data-stu-id="12a1b-109">These probabilities may not be normalized, but must all be non-negative.</span></span>



## <a name="output--discretedistribution"></a><span data-ttu-id="12a1b-110">Saída: [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="12a1b-110">Output : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="12a1b-111">O índice `i` com probabilidade `probs[i] / sum` , em que `sum` é a soma de `probs` fornecida por `Fold(PlusD, 0.0, probs)` .</span><span class="sxs-lookup"><span data-stu-id="12a1b-111">The index `i` with probability `probs[i] / sum`, where `sum` is the sum of `probs` given by `Fold(PlusD, 0.0, probs)`.</span></span>