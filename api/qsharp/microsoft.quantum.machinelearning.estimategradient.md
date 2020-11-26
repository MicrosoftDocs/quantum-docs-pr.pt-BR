---
uid: Microsoft.Quantum.MachineLearning.EstimateGradient
title: Operação EstimateGradient
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateGradient
qsharp.summary: Estimates the training gradient for a sequential classifier at a particular model and for a given encoded input.
ms.openlocfilehash: 79f4abdf131509d4948a3c114e631118329f88d8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211841"
---
# <a name="estimategradient-operation"></a>Operação EstimateGradient

Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Estima o gradiente de treinamento para um classificador sequencial em um modelo específico e para uma determinada entrada codificada.

```qsharp
operation EstimateGradient (model : Microsoft.Quantum.MachineLearning.SequentialModel, encodedInput : Microsoft.Quantum.MachineLearning.StateGenerator, nMeasurements : Int) : Double[]
```


## <a name="input"></a>Entrada

### <a name="model--sequentialmodel"></a>modelo: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)

O modelo sequencial cujo gradiente deve ser estimado.


### <a name="encodedinput--stategenerator"></a>encodedInput: [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)

Uma entrada para o classificador sequencial, codificada em uma operação de preparação de estado.


### <a name="nmeasurements--int"></a>nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)

O número de medições a serem usadas na estimativa do gradiente.



## <a name="output--double"></a>Saída: [Double](xref:microsoft.quantum.lang-ref.double)[]

Uma estimativa do gradiente de treinamento nos parâmetros de entrada e modelo especificados.

## <a name="remarks"></a>Comentários

Essa operação usa um teste Hadamard e a técnica Shift de parâmetro em conjunto para estimar o gradiente.