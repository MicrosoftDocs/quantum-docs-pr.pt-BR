---
uid: Microsoft.Quantum.MachineLearning.Sampled
title: Função de amostra
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Sampled
qsharp.summary: Samples a given array, using the given schedule.
ms.openlocfilehash: 5dd599246847718f4f0411715585cb416595db9d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854942"
---
# <a name="sampled-function"></a>Função de amostra

Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


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

