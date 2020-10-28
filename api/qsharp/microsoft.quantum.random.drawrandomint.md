---
uid: Microsoft.Quantum.Random.DrawRandomInt
title: Operação DrawRandomInt
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomInt
qsharp.summary: Draws a random integer in a given inclusive range.
ms.openlocfilehash: d9d8d9fbb25587ac5ccbd4edf0e555649380375f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696974"
---
# <a name="drawrandomint-operation"></a>Operação DrawRandomInt

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Agrupa [](https://nuget.org/packages/)


Desenha um inteiro aleatório em um determinado intervalo inclusivo.

```qsharp
operation DrawRandomInt (min : Int, max : Int) : Int
```


## <a name="input"></a>Entrada

### <a name="min--int"></a>mín.: [int](xref:microsoft.quantum.lang-ref.int)

O menor inteiro a ser desenhado.


### <a name="max--int"></a>máx.: [int](xref:microsoft.quantum.lang-ref.int)

O maior inteiro a ser desenhado.



## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)

Um número inteiro no intervalo inclusivo de `min` a `max` com probabilidade uniforme.

## <a name="remarks"></a>Comentários

Falha se `max <= min` .

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. DiscreteUniformDistribution](xref:Microsoft.Quantum.DiscreteUniformDistribution)