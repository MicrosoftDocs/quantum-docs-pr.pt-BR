---
uid: Microsoft.Quantum.MachineLearning._RunSingleTrainingEpoch
title: _RunSingleTrainingEpoch operação
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: _RunSingleTrainingEpoch
qsharp.summary: Perform one epoch of sequential classifier training on a subset of data samples.
ms.openlocfilehash: 71780645a025972f11f32f8ba8fd94d098604f9e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196745"
---
# <a name="_runsingletrainingepoch-operation"></a>_RunSingleTrainingEpoch operação

Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Execute uma época de treinamento sequencial de classificador em um subconjunto de exemplos de dados.

```qsharp
operation _RunSingleTrainingEpoch (encodedSamples : (Microsoft.Quantum.MachineLearning.LabeledSample, Microsoft.Quantum.MachineLearning.StateGenerator)[], schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, periodScore : Int, options : Microsoft.Quantum.MachineLearning.TrainingOptions, model : Microsoft.Quantum.MachineLearning.SequentialModel, nPreviousBestMisses : Int) : (Int, Microsoft.Quantum.MachineLearning.SequentialModel)
```


## <a name="input"></a>Entrada

### <a name="encodedsamples--labeledsamplestategenerator"></a>encodedSamples: ([LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample),[StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)) []




### <a name="schedule--samplingschedule"></a>agendamento: [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)




### <a name="periodscore--int"></a>periodScore: [int](xref:microsoft.quantum.lang-ref.int)

O número de etapas de gradiente a serem seguidas entre pontos de pontuação.
Para obter a melhor precisão, defina como 1.


### <a name="options--trainingoptions"></a>opções: [trainoptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)

Opções a serem usadas no treinamento.


### <a name="model--sequentialmodel"></a>modelo: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)

O modelo sequencial a ser treinado.


### <a name="npreviousbestmisses--int"></a>nPreviousBestMisses: [int](xref:microsoft.quantum.lang-ref.int)

O melhor número de classificações incorretas observadas nas épocas anteriores.



## <a name="output--intsequentialmodel"></a>Saída: ([int](xref:microsoft.quantum.lang-ref.int),[SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel))

- O menor número de classificações incorretas observadas até essa época.
- O novo modelo melhor sequencial encontrado.