---
uid: Microsoft.Quantum.MachineLearning.InferredLabel
title: Função InferredLabel
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabel
qsharp.summary: Given a of classification probability and a bias, returns the label inferred from that probability.
ms.openlocfilehash: b64bb1ec52d2456ee1b627b920890223d173533b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211773"
---
# <a name="inferredlabel-function"></a>Função InferredLabel

Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Devido a uma probabilidade de classificação e uma tendência, retorna o rótulo inferido da probabilidade.

```qsharp
function InferredLabel (bias : Double, probability : Double) : Int
```


## <a name="input"></a>Entrada

### <a name="bias--double"></a>tendência: [duplo](xref:microsoft.quantum.lang-ref.double)

A tendência entre duas classes, geralmente o resultado do treinamento de um classificador.


### <a name="probability--double"></a>probabilidade: [Double](xref:microsoft.quantum.lang-ref.double)

As probabilidades de classificação para um exemplo específico, normalmente resultando da estimativa da sua frequência de classificação.



## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)

O rótulo inferido da probabilidade de classificação fornecida.