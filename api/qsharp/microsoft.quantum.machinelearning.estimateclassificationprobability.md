---
uid: Microsoft.Quantum.MachineLearning.EstimateClassificationProbability
title: Operação EstimateClassificationProbability
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateClassificationProbability
qsharp.summary: Given a sample and a sequential classifier, estimates the classification probability for that sample by repeatedly measuring the output of the classifier on the given sample.
ms.openlocfilehash: c2b74bc55ad9005a8f52d05796e856f4f2fb62ba
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853949"
---
# <a name="estimateclassificationprobability-operation"></a>Operação EstimateClassificationProbability

Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Dada uma amostra e um classificador sequencial, estima a probabilidade de classificação para esse exemplo medindo repetidamente a saída do classificador no exemplo fornecido.

```qsharp
operation EstimateClassificationProbability (tolerance : Double, model : Microsoft.Quantum.MachineLearning.SequentialModel, sample : Double[], nMeasurements : Int) : Double
```


## <a name="input"></a>Entrada

### <a name="tolerance--double"></a>tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)

A tolerância para permitir a codificação da amostra em uma operação de preparação de estado.


### <a name="model--sequentialmodel"></a>modelo: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)

O modelo sequencial a ser usado para estimar a probabilidade de classificação para o exemplo fornecido.


### <a name="sample--double"></a>exemplo: [Double](xref:microsoft.quantum.lang-ref.double)[]

O vetor de recurso para o exemplo a ser classificado.


### <a name="nmeasurements--int"></a>nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)

O número de medições a serem usadas na estimativa da probabilidade de classificação.



## <a name="output--double"></a>Saída: [duplo](xref:microsoft.quantum.lang-ref.double)

Uma estimativa da probabilidade de classificação para o exemplo fornecido.