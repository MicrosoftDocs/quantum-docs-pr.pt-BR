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
# <a name="categoricaldistribution-function"></a>Função CategoricalDistribution

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Agrupa [](https://nuget.org/packages/)


Retorna uma distribuição categórica discreta, na qual a probabilidade de cada uma lista finita de resultados determinados é especificada explicitamente.

```qsharp
function CategoricalDistribution (probs : Double[]) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a>Entrada

### <a name="probs--double"></a>Probes: [Double](xref:microsoft.quantum.lang-ref.double)[]

As probabilidades para cada resultado da distribuição categórica.
Essas probabilidades não podem ser normalizadas, mas devem ser não negativas.



## <a name="output--discretedistribution"></a>Saída: [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)

O índice `i` com probabilidade `probs[i] / sum` , em que `sum` é a soma de `probs` fornecida por `Fold(PlusD, 0.0, probs)` .