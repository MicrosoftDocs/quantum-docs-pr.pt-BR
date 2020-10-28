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
# <a name="sampled-function"></a><span data-ttu-id="9a70a-102">Função de amostra</span><span class="sxs-lookup"><span data-stu-id="9a70a-102">Sampled function</span></span>

<span data-ttu-id="9a70a-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="9a70a-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="9a70a-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9a70a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9a70a-105">Amostras de uma determinada matriz, usando o agendamento fornecido.</span><span class="sxs-lookup"><span data-stu-id="9a70a-105">Samples a given array, using the given schedule.</span></span>

```qsharp
function Sampled<'T> (schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, values : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="9a70a-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="9a70a-106">Input</span></span>

### <a name="schedule--samplingschedule"></a><span data-ttu-id="9a70a-107">agendamento: [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="9a70a-107">schedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="9a70a-108">Um agendamento a ser usado em valores de amostragem.</span><span class="sxs-lookup"><span data-stu-id="9a70a-108">A schedule to use in sampling values.</span></span>


### <a name="values--t"></a><span data-ttu-id="9a70a-109">valores: ' T' []</span><span class="sxs-lookup"><span data-stu-id="9a70a-109">values : 'T[]</span></span>

<span data-ttu-id="9a70a-110">Uma matriz de valores a serem amostrados.</span><span class="sxs-lookup"><span data-stu-id="9a70a-110">An array of values to be sampled.</span></span>



## <a name="output--t"></a><span data-ttu-id="9a70a-111">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="9a70a-111">Output : 'T[]</span></span>

<span data-ttu-id="9a70a-112">Uma matriz de elementos de valores, seguindo o agendamento fornecido.</span><span class="sxs-lookup"><span data-stu-id="9a70a-112">An array of elements from values, following the given schedule.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="9a70a-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="9a70a-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9a70a-114">T'</span><span class="sxs-lookup"><span data-stu-id="9a70a-114">'T</span></span>

