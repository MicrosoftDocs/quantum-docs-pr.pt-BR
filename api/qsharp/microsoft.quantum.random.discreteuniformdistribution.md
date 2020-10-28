---
uid: Microsoft.Quantum.Random.DiscreteUniformDistribution
title: Função DiscreteUniformDistribution
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DiscreteUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive range.
ms.openlocfilehash: 5e93c66d891d9b6aec548c0cf266df35e6090c92
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694647"
---
# <a name="discreteuniformdistribution-function"></a>Função DiscreteUniformDistribution

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Agrupa [](https://nuget.org/packages/)


Retorna uma distribuição uniforme em um determinado intervalo inclusivo.

```qsharp
function DiscreteUniformDistribution (min : Int, max : Int) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a>Entrada

### <a name="min--int"></a>mín.: [int](xref:microsoft.quantum.lang-ref.int)

O menor inteiro a ser desenhado.


### <a name="max--int"></a>máx.: [int](xref:microsoft.quantum.lang-ref.int)

O maior inteiro a ser desenhado.



## <a name="output--discretedistribution"></a>Saída: [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)

Uma distribuição cujos variates aleatórios são inteiros no intervalo inclusivo de `min` a `max` com probabilidade uniforme.

## <a name="remarks"></a>Comentários

Falha se `max <= min` .

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. DrawRandomDouble](xref:Microsoft.Quantum.DrawRandomDouble)