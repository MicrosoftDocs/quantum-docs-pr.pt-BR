---
uid: Microsoft.Quantum.Random.NormalDistribution
title: Função NormalDistribution
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: NormalDistribution
qsharp.summary: Returns a normal distribution with a given mean and variance.
ms.openlocfilehash: 733a2763dca6d75f81d538f63c3084331a8e1d51
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98814179"
---
# <a name="normaldistribution-function"></a>Função NormalDistribution

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Retorna uma distribuição normal com uma determinada média e variância.

```qsharp
function NormalDistribution (mean : Double, variance : Double) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a>Entrada

### <a name="mean--double"></a>média: [duplo](xref:microsoft.quantum.lang-ref.double)




### <a name="variance--double"></a>variância: [Double](xref:microsoft.quantum.lang-ref.double)





## <a name="output--continuousdistribution"></a>Saída: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)



## <a name="example"></a>Exemplo

O seguinte desenha 10 amostras da distribuição normal com média 2 e desvio padrão 0,1:

```qsharp
let samples = DrawMany(
    (NormalDistribution(2.0, PowD(0.1, 2.0)))::Sample,
    10, ()
);
```

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Random. StandardNormalDistribution](xref:Microsoft.Quantum.Random.StandardNormalDistribution)