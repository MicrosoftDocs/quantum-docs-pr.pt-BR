---
uid: Microsoft.Quantum.Random.MaybeChooseElement
title: Operação MaybeChooseElement
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: MaybeChooseElement
qsharp.summary: Given an array of data and an a distribution over its indices, attempts to choose an element at random.
ms.openlocfilehash: 1a69c8d5a6ae022ceda9269e17434b740809b107
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192852"
---
# <a name="maybechooseelement-operation"></a>Operação MaybeChooseElement

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Dada uma matriz de dados e uma distribuição sobre seus índices, o tenta escolher um elemento aleatoriamente.

```qsharp
operation MaybeChooseElement<'T> (data : 'T[], indexDistribution : Microsoft.Quantum.Random.DiscreteDistribution) : (Bool, 'T)
```


## <a name="input"></a>Entrada

### <a name="data--t"></a>dados: ' t []

A matriz da qual um elemento deve ser escolhido.


### <a name="indexdistribution--discretedistribution"></a>indexDistribution: [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)

Uma distribuição nos índices de `data` .



## <a name="output--boolt"></a>Saída: ([bool](xref:microsoft.quantum.lang-ref.bool), não)



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

