---
uid: Microsoft.Quantum.Random.ContinuousUniformDistribution
title: Função ContinuousUniformDistribution
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: ContinuousUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive interval.
ms.openlocfilehash: 74300efb10ba7b5aa006f0b1b6aafde0da840f00
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693045"
---
# <a name="continuousuniformdistribution-function"></a>Função ContinuousUniformDistribution

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Agrupa [](https://nuget.org/packages/)


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