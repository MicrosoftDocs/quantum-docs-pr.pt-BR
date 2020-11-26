---
uid: Microsoft.Quantum.MachineLearning.Sampled
title: Função de amostra
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Sampled
qsharp.summary: Samples a given array, using the given schedule.
ms.openlocfilehash: ddff72bbed6f20e8e0ceb3bfe3fc50a3da0bd2a9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211620"
---
# <a name="sampled-function"></a><span data-ttu-id="07850-102">Função de amostra</span><span class="sxs-lookup"><span data-stu-id="07850-102">Sampled function</span></span>

<span data-ttu-id="07850-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="07850-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="07850-104">Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="07850-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="07850-105">Amostras de uma determinada matriz, usando o agendamento fornecido.</span><span class="sxs-lookup"><span data-stu-id="07850-105">Samples a given array, using the given schedule.</span></span>

```qsharp
function Sampled<'T> (schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, values : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="07850-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="07850-106">Input</span></span>

### <a name="schedule--samplingschedule"></a><span data-ttu-id="07850-107">agendamento: [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="07850-107">schedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="07850-108">Um agendamento a ser usado em valores de amostragem.</span><span class="sxs-lookup"><span data-stu-id="07850-108">A schedule to use in sampling values.</span></span>


### <a name="values--t"></a><span data-ttu-id="07850-109">valores: ' T' []</span><span class="sxs-lookup"><span data-stu-id="07850-109">values : 'T[]</span></span>

<span data-ttu-id="07850-110">Uma matriz de valores a serem amostrados.</span><span class="sxs-lookup"><span data-stu-id="07850-110">An array of values to be sampled.</span></span>



## <a name="output--t"></a><span data-ttu-id="07850-111">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="07850-111">Output : 'T[]</span></span>

<span data-ttu-id="07850-112">Uma matriz de elementos de valores, seguindo o agendamento fornecido.</span><span class="sxs-lookup"><span data-stu-id="07850-112">An array of elements from values, following the given schedule.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="07850-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="07850-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="07850-114">T'</span><span class="sxs-lookup"><span data-stu-id="07850-114">'T</span></span>

