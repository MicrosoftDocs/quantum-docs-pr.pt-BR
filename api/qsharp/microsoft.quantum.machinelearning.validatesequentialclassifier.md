---
uid: Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier
title: Operação ValidateSequentialClassifier
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ValidateSequentialClassifier
qsharp.summary: Validates a given sequential classifier against a given set of pre-labeled samples.
ms.openlocfilehash: c100c5786b18996ce13067f1c4618cf0189578f5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848971"
---
# <a name="validatesequentialclassifier-operation"></a>Operação ValidateSequentialClassifier

Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


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