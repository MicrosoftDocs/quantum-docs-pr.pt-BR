---
uid: Microsoft.Quantum.MachineLearning.TrainingOptions
title: Tipo definido pelo usuário trainoptions
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: TrainingOptions
qsharp.summary: A collection of options to be used in training quantum classifiers.
ms.openlocfilehash: 762d6853910832c6d4cda522c0c5df706d1ed195
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842777"
---
# <a name="trainingoptions-user-defined-type"></a>Tipo definido pelo usuário trainoptions

Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Uma coleção de opções a ser usada em classificadores do quantum de treinamento.

```qsharp

newtype TrainingOptions = (LearningRate : Double, Tolerance : Double, MinibatchSize : Int, NMeasurements : Int, MaxEpochs : Int, MaxStalls : Int, StochasticRescaleFactor : Double, ScoringPeriod : Int, VerboseMessage : (String -> Unit));
```



## <a name="named-items"></a>Itens nomeados

### <a name="learningrate--double"></a>LearningRate: [Double](xref:microsoft.quantum.lang-ref.double)

A taxa de aprendizagem pela qual os gradientes devem ser redimensionados ao atualizar os parâmetros do modelo durante as etapas de treinamento.
### <a name="tolerance--double"></a>Tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)

A tolerância a aproximação a ser usada ao preparar exemplos como Estados de Quantum.
### <a name="minibatchsize--int"></a>MinibatchSize: [int](xref:microsoft.quantum.lang-ref.int)

O número de amostras a serem usadas em cada minilote de treinamento.
### <a name="nmeasurements--int"></a>NMeasurements: [int](xref:microsoft.quantum.lang-ref.int)

O número de vezes para medir cada resultado de classificação a fim de estimar a probabilidade de classificação.
### <a name="maxepochs--int"></a>MaxEpochs: [int](xref:microsoft.quantum.lang-ref.int)

O número máximo de épocas para treinar cada modelo.
### <a name="maxstalls--int"></a>MaxStalls: [int](xref:microsoft.quantum.lang-ref.int)

O número máximo de vezes que uma época de treinamento tem permissão para paralisar (aproximadamente zero gradiente) antes de falhar.
### <a name="stochasticrescalefactor--double"></a>StochasticRescaleFactor: [Double](xref:microsoft.quantum.lang-ref.double)

O valor para redimensionar os modelos interrompidos antes de tentar novamente uma atualização.
### <a name="scoringperiod--int"></a>ScoringPeriod: [int](xref:microsoft.quantum.lang-ref.int)

O número de etapas de gradiente a serem seguidas entre pontos de pontuação.
Para obter a melhor precisão, defina como 1.
### <a name="verbosemessage--string---unit"></a>VerboseMessage: unidade de [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string) -> [](xref:microsoft.quantum.lang-ref.unit)

Uma função que pode ser usada para fornecer comentários detalhados.

## <a name="remarks"></a>Comentários

Esse UDT não deve ser criado diretamente, mas deve ser especificado chamando @"microsoft.quantum.machinelearning.defaulttrainingoptions" e, em seguida, usando o `w/` operador para substituir os padrões diferentes.

Por exemplo, para usar medidas de 100.000 e no máximo 8 épocas de treinamento:

```qsharp
let options = DefaultTrainingOptions()
              w/ NMeasurements <- 100000
              w/ MaxEpochs <- 8;
```

## <a name="references"></a>Referências

- [arXiv:1804.00633](https://arxiv.org/abs/1804.00633)