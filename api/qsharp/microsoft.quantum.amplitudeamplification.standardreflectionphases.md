---
uid: Microsoft.Quantum.AmplitudeAmplification.StandardReflectionPhases
title: Função StandardReflectionPhases
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: StandardReflectionPhases
qsharp.summary: Computes partial reflection phases for standard amplitude amplification.
ms.openlocfilehash: 703b50d0186cd0f4eddb9a29fa3cffb2b746c8d6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843911"
---
# <a name="standardreflectionphases-function"></a><span data-ttu-id="79730-102">Função StandardReflectionPhases</span><span class="sxs-lookup"><span data-stu-id="79730-102">StandardReflectionPhases function</span></span>

<span data-ttu-id="79730-103">Namespace: [Microsoft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="79730-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="79730-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="79730-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="79730-105">Computa fases de reflexo parcial para amplificação de amplitude padrão.</span><span class="sxs-lookup"><span data-stu-id="79730-105">Computes partial reflection phases for standard amplitude amplification.</span></span>

```qsharp
function StandardReflectionPhases (nIterations : Int) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a><span data-ttu-id="79730-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="79730-106">Input</span></span>

### <a name="niterations--int"></a><span data-ttu-id="79730-107">nIterations: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="79730-107">nIterations : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="79730-108">Número de iterações de amplificação de amplitude para as quais gerar fases de reflexo parcial.</span><span class="sxs-lookup"><span data-stu-id="79730-108">Number of amplitude amplification iterations to generate partial reflection phases for.</span></span>



## <a name="output--reflectionphases"></a><span data-ttu-id="79730-109">Saída: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="79730-109">Output : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="79730-110">Uma operação que implementa as fases especificadas como reflexos parciais</span><span class="sxs-lookup"><span data-stu-id="79730-110">An operation that implements phases specified as partial reflections</span></span>

## <a name="remarks"></a><span data-ttu-id="79730-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="79730-111">Remarks</span></span>

<span data-ttu-id="79730-112">Todas as fases são $ \pi $, exceto a primeira reflexão sobre o estado de início e a última reflexão sobre o estado de destino, que são $0 $.</span><span class="sxs-lookup"><span data-stu-id="79730-112">All phases are $\pi$, except for the first reflection about the start state and the last reflection about the target state, which are $0$.</span></span>