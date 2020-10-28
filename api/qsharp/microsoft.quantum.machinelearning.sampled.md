---
uid: Microsoft.Quantum.MachineLearning.Sampled
title: Função de amostra
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Sampled
qsharp.summary: Samples a given array, using the given schedule.
ms.openlocfilehash: 9f9f91bc50861c5b31a76e28050189d13efda71e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694985"
---
# <a name="sampled-function"></a>Função de amostra

Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Agrupa [](https://nuget.org/packages/)


Amostras de uma determinada matriz, usando o agendamento fornecido.

```qsharp
function Sampled<'T> (schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, values : 'T[]) : 'T[]
```


## <a name="input"></a>Entrada

### <a name="schedule--samplingschedule"></a>agendamento: [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)

Um agendamento a ser usado em valores de amostragem.


### <a name="values--t"></a>valores: ' T' []

Uma matriz de valores a serem amostrados.



## <a name="output--t"></a>Saída: ' T' []

Uma matriz de elementos de valores, seguindo o agendamento fornecido.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

