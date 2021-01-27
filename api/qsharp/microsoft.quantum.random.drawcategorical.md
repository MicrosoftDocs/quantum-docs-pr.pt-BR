---
uid: Microsoft.Quantum.Random.DrawCategorical
title: Operação DrawCategorical
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawCategorical
qsharp.summary: Draws a random sample from a categorical distribution specified by a list of probablities.
ms.openlocfilehash: a9fe1b08e80abc65a5c4b803f0cb8a5e7a62759c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851163"
---
# <a name="drawcategorical-operation"></a>Operação DrawCategorical

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Desenha um exemplo aleatório de uma distribuição categórica especificada por uma lista de probablities.

```qsharp
operation DrawCategorical (probs : Double[]) : Int
```


## <a name="description"></a>Descrição

A probabilidade de selecionar um índice específico é proporcional ao valor do elemento de matriz nesse índice.
Os elementos de matriz que são iguais a zero são ignorados e seus índices nunca são retornados. Se qualquer elemento de matriz for menor que zero, ou se nenhum elemento de matriz for maior que zero, a operação falhará.

## <a name="input"></a>Entrada

### <a name="probs--double"></a>Probes: [Double](xref:microsoft.quantum.lang-ref.double)[]

Uma matriz de números de ponto flutuante proporcional à probabilidade de selecionar cada índice.



## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)

Um inteiro $i $ com probabilidade $ \Pr (i) = p_i/\ sum_i p_i $, em que $p _i $ é o elemento $i $ th de `probs` .

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Random. CategoricalDistribution](xref:Microsoft.Quantum.Random.CategoricalDistribution)