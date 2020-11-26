---
uid: Microsoft.Quantum.Random.DrawRandomInt
title: Operação DrawRandomInt
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomInt
qsharp.summary: Draws a random integer in a given inclusive range.
ms.openlocfilehash: f7b6cb75f761e4c45295245ed4bd4fb82c592809
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192903"
---
# <a name="drawrandomint-operation"></a>Operação DrawRandomInt

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


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