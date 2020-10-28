---
uid: Microsoft.Quantum.MachineLearning.InferredLabels
title: Função InferredLabels
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabels
qsharp.summary: Given an array of classification probabilities and a bias, returns the label inferred from each probability.
ms.openlocfilehash: 874d1a2f7cc6d67567e0d2baa70b0d26b639a029
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694993"
---
# <a name="inferredlabels-function"></a>Função InferredLabels

Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Agrupa [](https://nuget.org/packages/)


Dada uma matriz de probabilidades de classificação e uma tendência, retorna o rótulo inferido de cada probabilidade.

```qsharp
function InferredLabels (bias : Double, probabilities : Double[]) : Int[]
```


## <a name="input"></a>Entrada

### <a name="bias--double"></a>tendência: [duplo](xref:microsoft.quantum.lang-ref.double)

A tendência entre duas classes, geralmente o resultado do treinamento de um classificador.


### <a name="probabilities--double"></a>probabilidades: [Double](xref:microsoft.quantum.lang-ref.double)[]

Uma matriz de probabilidades de classificação para um conjunto de amostras, normalmente resultante da estimativa de frequências de classificação.



## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)[]

O rótulo inferido de cada probabilidade de classificação.