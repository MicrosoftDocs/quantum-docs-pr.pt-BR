---
uid: Microsoft.Quantum.MachineLearning.ScheduleLength
title: Função ScheduleLength
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ScheduleLength
qsharp.summary: Returns the number of elements in a given sampling schedule.
ms.openlocfilehash: 77538984fbd7334712df423b991ef43ce31ed849
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694982"
---
# <a name="schedulelength-function"></a>Função ScheduleLength

Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Agrupa [](https://nuget.org/packages/)


Retorna o número de elementos em um determinado agendamento de amostragem.

```qsharp
function ScheduleLength (schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : Int
```


## <a name="input"></a>Entrada

### <a name="schedule--samplingschedule"></a>agendamento: [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)

Um agendamento de amostragem cujo comprimento deve ser retornado.



## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)

O número de elementos no agendamento de amostragem fornecido.