---
uid: Microsoft.Quantum.MachineLearning.ScheduleLength
title: Função ScheduleLength
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ScheduleLength
qsharp.summary: Returns the number of elements in a given sampling schedule.
ms.openlocfilehash: 008bdcdc0a7c0ad2775dea65ebba46556092beed
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211586"
---
# <a name="schedulelength-function"></a>Função ScheduleLength

Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Retorna o número de elementos em um determinado agendamento de amostragem.

```qsharp
function ScheduleLength (schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : Int
```


## <a name="input"></a>Entrada

### <a name="schedule--samplingschedule"></a>agendamento: [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)

Um agendamento de amostragem cujo comprimento deve ser retornado.



## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)

O número de elementos no agendamento de amostragem fornecido.