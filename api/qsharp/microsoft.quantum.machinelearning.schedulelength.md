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
# <a name="schedulelength-function"></a><span data-ttu-id="fd988-102">Função ScheduleLength</span><span class="sxs-lookup"><span data-stu-id="fd988-102">ScheduleLength function</span></span>

<span data-ttu-id="fd988-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="fd988-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="fd988-104">Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="fd988-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="fd988-105">Retorna o número de elementos em um determinado agendamento de amostragem.</span><span class="sxs-lookup"><span data-stu-id="fd988-105">Returns the number of elements in a given sampling schedule.</span></span>

```qsharp
function ScheduleLength (schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : Int
```


## <a name="input"></a><span data-ttu-id="fd988-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="fd988-106">Input</span></span>

### <a name="schedule--samplingschedule"></a><span data-ttu-id="fd988-107">agendamento: [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="fd988-107">schedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="fd988-108">Um agendamento de amostragem cujo comprimento deve ser retornado.</span><span class="sxs-lookup"><span data-stu-id="fd988-108">A sampling schedule whose length is to be returned.</span></span>



## <a name="output--int"></a><span data-ttu-id="fd988-109">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="fd988-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="fd988-110">O número de elementos no agendamento de amostragem fornecido.</span><span class="sxs-lookup"><span data-stu-id="fd988-110">The number of elements in the given sampling schedule.</span></span>