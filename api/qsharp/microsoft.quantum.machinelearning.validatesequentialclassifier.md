---
uid: Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier
title: Operação ValidateSequentialClassifier
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ValidateSequentialClassifier
qsharp.summary: Validates a given sequential classifier against a given set of pre-labeled samples.
ms.openlocfilehash: 802f1045ea4086bd371d68018a481182cb75b209
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694672"
---
# <a name="validatesequentialclassifier-operation"></a>Operação ValidateSequentialClassifier

Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Agrupa [](https://nuget.org/packages/)


Valida um classificador sequencial fornecido em relação a um determinado conjunto de amostras previamente rotuladas.

```qsharp
operation ValidateSequentialClassifier (model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Microsoft.Quantum.MachineLearning.LabeledSample[], tolerance : Double, nMeasurements : Int, validationSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : Microsoft.Quantum.MachineLearning.ValidationResults
```


## <a name="input"></a>Entrada

### <a name="model--sequentialmodel"></a>modelo: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)

O modelo sequencial a ser validado.


### <a name="samples--labeledsample"></a>exemplos: [LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]

Os exemplos a serem usados para validar o modelo fornecido.


### <a name="tolerance--double"></a>tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)

A tolerância a aproximação a ser usada na codificação de cada amostra como uma entrada para o classificador sequencial.


### <a name="nmeasurements--int"></a>nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)

O número de medições a serem usadas na classificação de cada amostra.


### <a name="validationschedule--samplingschedule"></a>validationSchedule: [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)

O agendamento pelo qual os exemplos devem ser extraídos do conjunto de validação.



## <a name="output--validationresults"></a>Saída: [ValidationResults](xref:Microsoft.Quantum.MachineLearning.ValidationResults)

Os resultados da validação fornecida.