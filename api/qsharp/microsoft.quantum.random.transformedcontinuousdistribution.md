---
uid: Microsoft.Quantum.Random.TransformedContinuousDistribution
title: Função TransformedContinuousDistribution
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: TransformedContinuousDistribution
qsharp.summary: Given a continuous distribution, returns a new distribution that transforms the original by a given function.
ms.openlocfilehash: 6a6e0c26bd650fd4c05208197ff23f951d1c3b5c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693261"
---
# <a name="transformedcontinuousdistribution-function"></a>Função TransformedContinuousDistribution

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Agrupa [](https://nuget.org/packages/)


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