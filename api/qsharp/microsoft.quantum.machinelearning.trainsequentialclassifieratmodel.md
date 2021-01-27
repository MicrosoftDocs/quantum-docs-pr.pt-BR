---
uid: Microsoft.Quantum.MachineLearning.TrainSequentialClassifierAtModel
title: Operação TrainSequentialClassifierAtModel
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: TrainSequentialClassifierAtModel
qsharp.summary: Given the structure of a sequential classifier, trains the classifier on a given labeled training set, starting from a particular model.
ms.openlocfilehash: 4164c190cb19b6d3ea74d9803a77d2b19607279b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857152"
---
# <a name="trainsequentialclassifieratmodel-operation"></a>Operação TrainSequentialClassifierAtModel

Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Dada a estrutura de um classificador sequencial, treina o classificador em um determinado conjunto de treinamento rotulado, começando com um modelo específico.

```qsharp
operation TrainSequentialClassifierAtModel (model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Microsoft.Quantum.MachineLearning.LabeledSample[], options : Microsoft.Quantum.MachineLearning.TrainingOptions, trainingSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, validationSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : (Microsoft.Quantum.MachineLearning.SequentialModel, Int)
```


## <a name="input"></a>Entrada

### <a name="model--sequentialmodel"></a>modelo: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)

O modelo sequencial a ser usado como ponto de partida para treinamento.


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

- [Microsoft. Quantum. MachineLearning. TrainSequentialClassifier](xref:Microsoft.Quantum.MachineLearning.TrainSequentialClassifier)
- [Microsoft. Quantum. MachineLearning. ValidateSequentialClassifier](xref:Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier)