---
uid: Microsoft.Quantum.Random.ContinuousUniformDistribution
title: Função ContinuousUniformDistribution
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: ContinuousUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive interval.
ms.openlocfilehash: a3911fe9962ce18daa239de0272c53d83344134a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193073"
---
# <a name="continuousuniformdistribution-function"></a>Função ContinuousUniformDistribution

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Retorna uma distribuição uniforme em um determinado intervalo inclusivo.

```qsharp
function ContinuousUniformDistribution (min : Double, max : Double) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a>Entrada

### <a name="min--double"></a>mín.: [duplo](xref:microsoft.quantum.lang-ref.double)

O menor número real a ser desenhado.


### <a name="max--double"></a>máx.: [duplo](xref:microsoft.quantum.lang-ref.double)

O maior número real a ser desenhado.



## <a name="output--continuousdistribution"></a>Saída: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)

Uma distribuição cujos variates aleatórios são números reais no intervalo inclusivo de `min` a `max` com probabilidade uniforme.

## <a name="remarks"></a>Comentários

Falha se `max <= min` .

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. DrawRandomDouble](xref:Microsoft.Quantum.DrawRandomDouble)