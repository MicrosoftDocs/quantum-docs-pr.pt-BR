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

## <a name="example"></a>Exemplo

O código Q # a seguir exibirá 0 com probabilidade 30% e 1 com probabilidade de 70%:

```qsharp
let dist = CategoricalDistribution([0.3, 0.7]);
Message($"Got sample: {dist::Sample()}");
```