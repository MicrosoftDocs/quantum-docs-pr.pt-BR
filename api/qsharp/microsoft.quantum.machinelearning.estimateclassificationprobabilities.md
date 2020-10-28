---
uid: Microsoft.Quantum.MachineLearning.EstimateClassificationProbabilities
title: Operação EstimateClassificationProbabilities
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateClassificationProbabilities
qsharp.summary: Given a set of samples and a sequential classifier, estimates the classification probability for those samples by repeatedly measuring the output of the classifier on each sample.
ms.openlocfilehash: 2b7845d39256f718cc3e415207b8a47b24620bdb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693096"
---
# <a name="estimateclassificationprobabilities-operation"></a>Operação EstimateClassificationProbabilities

Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Agrupa [](https://nuget.org/packages/)


Dado um conjunto de amostras e um classificador sequencial, o estima a probabilidade de classificação para esses exemplos medindo repetidamente a saída do classificador em cada amostra.

```qsharp
operation EstimateClassificationProbabilities (tolerance : Double, model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Double[][], nMeasurements : Int) : Double[]
```


## <a name="input"></a>Entrada

### <a name="tolerance--double"></a>tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)

A tolerância para permitir a codificação da amostra em uma operação de preparação de estado.


### <a name="model--sequentialmodel"></a>modelo: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)

O modelo sequencial a ser usado para estimar as probabilidades de classificação para os exemplos fornecidos.


### <a name="samples--double"></a>exemplos: [Double](xref:microsoft.quantum.lang-ref.double)[] []

Uma matriz de vetores de recurso para cada amostra a ser classificada.


### <a name="nmeasurements--int"></a>nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)

O número de medições a serem usadas na estimativa da probabilidade de classificação.



## <a name="output--double"></a>Saída: [Double](xref:microsoft.quantum.lang-ref.double)[]

Uma matriz de estimativas da probabilidade de classificação para cada amostra fornecida.