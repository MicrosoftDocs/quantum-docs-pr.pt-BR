---
uid: Microsoft.Quantum.Random.CategoricalDistribution
title: Função CategoricalDistribution
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: CategoricalDistribution
qsharp.summary: Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.
ms.openlocfilehash: 2e3d9b17939d5a9a5bc5e7d89a843e0ff5a848ba
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210243"
---
# <a name="categoricaldistribution-function"></a>Função CategoricalDistribution

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


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