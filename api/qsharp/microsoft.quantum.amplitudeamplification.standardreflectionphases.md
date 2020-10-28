---
uid: Microsoft.Quantum.AmplitudeAmplification.StandardReflectionPhases
title: Função StandardReflectionPhases
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: StandardReflectionPhases
qsharp.summary: Computes partial reflection phases for standard amplitude amplification.
ms.openlocfilehash: c189b34b641989ab458986fb3f2872759b949be5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694886"
---
# <a name="standardreflectionphases-function"></a><span data-ttu-id="806fc-102">Função StandardReflectionPhases</span><span class="sxs-lookup"><span data-stu-id="806fc-102">StandardReflectionPhases function</span></span>

<span data-ttu-id="806fc-103">Namespace: [Microsoft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="806fc-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="806fc-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="806fc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="806fc-105">Computa fases de reflexo parcial para amplificação de amplitude padrão.</span><span class="sxs-lookup"><span data-stu-id="806fc-105">Computes partial reflection phases for standard amplitude amplification.</span></span>

```qsharp
function StandardReflectionPhases (nIterations : Int) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a><span data-ttu-id="806fc-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="806fc-106">Input</span></span>

### <a name="niterations--int"></a><span data-ttu-id="806fc-107">nIterations: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="806fc-107">nIterations : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="806fc-108">Número de iterações de amplificação de amplitude para as quais gerar fases de reflexo parcial.</span><span class="sxs-lookup"><span data-stu-id="806fc-108">Number of amplitude amplification iterations to generate partial reflection phases for.</span></span>



## <a name="output--reflectionphases"></a><span data-ttu-id="806fc-109">Saída: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="806fc-109">Output : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="806fc-110">Uma operação que implementa as fases especificadas como reflexos parciais</span><span class="sxs-lookup"><span data-stu-id="806fc-110">An operation that implements phases specified as partial reflections</span></span>

## <a name="remarks"></a><span data-ttu-id="806fc-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="806fc-111">Remarks</span></span>

<span data-ttu-id="806fc-112">Todas as fases são $ \pi $, exceto a primeira reflexão sobre o estado de início e a última reflexão sobre o estado de destino, que são $0 $.</span><span class="sxs-lookup"><span data-stu-id="806fc-112">All phases are $\pi$, except for the first reflection about the start state and the last reflection about the target state, which are $0$.</span></span>