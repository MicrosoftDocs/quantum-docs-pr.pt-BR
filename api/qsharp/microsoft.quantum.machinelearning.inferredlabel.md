---
uid: Microsoft.Quantum.MachineLearning.InferredLabel
title: Função InferredLabel
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabel
qsharp.summary: Given a of classification probability and a bias, returns the label inferred from that probability.
ms.openlocfilehash: 46b24c283a01e6ac1c959ee4a6899591ee708ff7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848413"
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