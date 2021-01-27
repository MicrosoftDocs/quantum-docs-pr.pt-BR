---
uid: Microsoft.Quantum.Random.CategoricalDistribution
title: Função CategoricalDistribution
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: CategoricalDistribution
qsharp.summary: Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.
ms.openlocfilehash: 754ada71078bd5446f78885ace31d92dce6bf1a4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842357"
---
# <a name="categoricaldistribution-function"></a><span data-ttu-id="10517-102">Função CategoricalDistribution</span><span class="sxs-lookup"><span data-stu-id="10517-102">CategoricalDistribution function</span></span>

<span data-ttu-id="10517-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="10517-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="10517-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="10517-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="10517-105">Retorna uma distribuição categórica discreta, na qual a probabilidade de cada uma lista finita de resultados determinados é especificada explicitamente.</span><span class="sxs-lookup"><span data-stu-id="10517-105">Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.</span></span>

```qsharp
function CategoricalDistribution (probs : Double[]) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a><span data-ttu-id="10517-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="10517-106">Input</span></span>

### <a name="probs--double"></a><span data-ttu-id="10517-107">Probes: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="10517-107">probs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="10517-108">As probabilidades para cada resultado da distribuição categórica.</span><span class="sxs-lookup"><span data-stu-id="10517-108">The probabilities for each outcome from the categorical distribution.</span></span>
<span data-ttu-id="10517-109">Essas probabilidades não podem ser normalizadas, mas devem ser não negativas.</span><span class="sxs-lookup"><span data-stu-id="10517-109">These probabilities may not be normalized, but must all be non-negative.</span></span>



## <a name="output--discretedistribution"></a><span data-ttu-id="10517-110">Saída: [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="10517-110">Output : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="10517-111">O índice `i` com probabilidade `probs[i] / sum` , em que `sum` é a soma de `probs` fornecida por `Fold(PlusD, 0.0, probs)` .</span><span class="sxs-lookup"><span data-stu-id="10517-111">The index `i` with probability `probs[i] / sum`, where `sum` is the sum of `probs` given by `Fold(PlusD, 0.0, probs)`.</span></span>

## <a name="example"></a><span data-ttu-id="10517-112">Exemplo</span><span class="sxs-lookup"><span data-stu-id="10517-112">Example</span></span>

<span data-ttu-id="10517-113">O código Q # a seguir exibirá 0 com probabilidade 30% e 1 com probabilidade de 70%:</span><span class="sxs-lookup"><span data-stu-id="10517-113">The following Q# code will display 0 with probability 30% and 1 with probability 70%:</span></span>

```qsharp
let dist = CategoricalDistribution([0.3, 0.7]);
Message($"Got sample: {dist::Sample()}");
```