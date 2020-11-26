---
uid: Microsoft.Quantum.Random.DrawRandomDouble
title: Operação DrawRandomDouble
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomDouble
qsharp.summary: Draws a random real number in a given inclusive interval.
ms.openlocfilehash: d62416f4a222716edb9393fe4f43731d0e8aa9d3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192937"
---
# <a name="drawrandomdouble-operation"></a>Operação DrawRandomDouble

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Desenha um número real aleatório em um determinado intervalo inclusivo.

```qsharp
operation DrawRandomDouble (min : Double, max : Double) : Double
```


## <a name="input"></a>Entrada

### <a name="min--double"></a>mín.: [duplo](xref:microsoft.quantum.lang-ref.double)

O menor número real a ser desenhado.


### <a name="max--double"></a>máx.: [duplo](xref:microsoft.quantum.lang-ref.double)

O maior número real a ser desenhado.



## <a name="output--double"></a>Saída: [duplo](xref:microsoft.quantum.lang-ref.double)

Um número real aleatório no intervalo inclusivo de `min` a `max` com probabilidade uniforme.

## <a name="remarks"></a>Comentários

Falha se `max <= min` .

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. ContinuousUniformDistribution](xref:Microsoft.Quantum.ContinuousUniformDistribution)