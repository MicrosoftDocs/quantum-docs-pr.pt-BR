---
uid: Microsoft.Quantum.Random.TransformedContinuousDistribution
title: Função TransformedContinuousDistribution
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: TransformedContinuousDistribution
qsharp.summary: Given a continuous distribution, returns a new distribution that transforms the original by a given function.
ms.openlocfilehash: b317eaaa0ff0180ea5d240464c96d1c6b59c9c70
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226257"
---
# <a name="transformedcontinuousdistribution-function"></a>Função TransformedContinuousDistribution

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Dada uma distribuição contínua, retorna uma nova distribuição que transforma o original por uma determinada função.

```qsharp
function TransformedContinuousDistribution (transform : (Double -> Double), distribution : Microsoft.Quantum.Random.ContinuousDistribution) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a>Entrada

### <a name="transform--double---double"></a>transformação: [duplo](xref:microsoft.quantum.lang-ref.double) -> [duplo](xref:microsoft.quantum.lang-ref.double)

Uma função que transforma variates da distribuição original para a distribuição transformada.


### <a name="distribution--continuousdistribution"></a>distribuição: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)

A distribuição original a ser transformada.



## <a name="output--continuousdistribution"></a>Saída: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)

Uma nova distribuição relacionada à `distribution` transformação fornecida pelo `transform` .