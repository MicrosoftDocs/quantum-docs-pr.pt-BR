---
uid: Microsoft.Quantum.MachineLearning.TrainSequentialClassifier
title: Operação TrainSequentialClassifier
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: TrainSequentialClassifier
qsharp.summary: Given the structure of a sequential classifier, trains the classifier on a given labeled training set.
ms.openlocfilehash: 12c4df59941b682d9de798e6585b59d1c34924dc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693313"
---
# <a name="trainsequentialclassifier-operation"></a>Operação TrainSequentialClassifier

Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Agrupa [](https://nuget.org/packages/)


Dada a estrutura de um classificador sequencial, treina o classificador em um determinado conjunto de treinamento rotulado.

```qsharp
operation TrainSequentialClassifier (models : Microsoft.Quantum.MachineLearning.SequentialModel[], samples : Microsoft.Quantum.MachineLearning.LabeledSample[], options : Microsoft.Quantum.MachineLearning.TrainingOptions, trainingSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, validationSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : (Microsoft.Quantum.MachineLearning.SequentialModel, Int)
```


## <a name="input"></a>Entrada

### <a name="models--sequentialmodel"></a>modelos: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)[]

Uma matriz de modelos a ser usada como pontos de partida durante o treinamento.


### <a name="samples--labeledsample"></a>exemplos: [LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]

Um conjunto de dados de treinamento rotulados que serão usados para executar o treinamento.


### <a name="options--trainingoptions"></a>opções: [trainoptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)

Configuração a ser usada durante o treinamento; consulte @"microsoft.quantum.machinelearning.trainingoptions" e @"microsoft.quantum.machinelearning.defaulttrainingoptions" para obter mais detalhes.


### <a name="trainingschedule--samplingschedule"></a>trainingSchedule: [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)

Um agendamento de amostragem a ser usado ao selecionar amostras dos dados de treinamento durante as etapas de treinamento.


### <a name="validationschedule--samplingschedule"></a>validationSchedule: [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)

Um agendamento de amostragem a ser usado ao selecionar amostras dos dados de treinamento ao selecionar qual ponto inicial resultou na melhor pontuação do classificador.



## <a name="output--sequentialmodelint"></a>Saída: ([SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel),[int](xref:microsoft.quantum.lang-ref.int))

- Uma parametrização do classificador fornecido e uma tendência entre as duas classes, em conjunto, correspondendo ao melhor resultado de cada um dos pontos de partida fornecidos.
- O número de erros observados no melhor modelo de classificador.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. MachineLearning. TrainSequentialClassifierAtModel](xref:Microsoft.Quantum.MachineLearning.TrainSequentialClassifierAtModel)
- [Microsoft. Quantum. MachineLearning. ValidateSequentialClassifier](xref:Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier)