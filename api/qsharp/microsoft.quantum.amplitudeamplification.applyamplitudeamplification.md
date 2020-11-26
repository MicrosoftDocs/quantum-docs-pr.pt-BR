---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyAmplitudeAmplification
title: Operação ApplyAmplitudeAmplification
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyAmplitudeAmplification
qsharp.summary: Applies amplitude amplification on a given register, using a given set of phases and oracles to reflect about the initial and final states.
ms.openlocfilehash: 0b40f94633bb43df5e64cd16d5ac8e12bcd1cc4a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191560"
---
# <a name="applyamplitudeamplification-operation"></a><span data-ttu-id="99049-102">Operação ApplyAmplitudeAmplification</span><span class="sxs-lookup"><span data-stu-id="99049-102">ApplyAmplitudeAmplification operation</span></span>

<span data-ttu-id="99049-103">Namespace: [Microsoft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="99049-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="99049-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="99049-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="99049-105">Aplica amplificação de amplitude em um determinado registro, usando um determinado conjunto de fases e ORACLES para refletir sobre os Estados inicial e final.</span><span class="sxs-lookup"><span data-stu-id="99049-105">Applies amplitude amplification on a given register, using a given set of phases and oracles to reflect about the initial and final states.</span></span>

```qsharp
operation ApplyAmplitudeAmplification (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, targetStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, target : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="99049-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="99049-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="99049-107">fases: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="99049-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="99049-108">Um conjunto de fases que descreve os reflexos parciais em cada etapa do algoritmo de amplificação de amplitude.</span><span class="sxs-lookup"><span data-stu-id="99049-108">A set of phases describing the partial reflections at each step of the amplitude amplification algorithm.</span></span> <span data-ttu-id="99049-109">Para ver um exemplo, consulte @"microsoft.quantum.amplitudeamplification.standardreflectionphases".</span><span class="sxs-lookup"><span data-stu-id="99049-109">See @"microsoft.quantum.amplitudeamplification.standardreflectionphases" for an example.</span></span>


### <a name="startstatereflection--reflectionoracle"></a><span data-ttu-id="99049-110">startStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="99049-110">startStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="99049-111">Um Oracle que reflete o estado inicial.</span><span class="sxs-lookup"><span data-stu-id="99049-111">An oracle that reflects about the initial state.</span></span>


### <a name="targetstatereflection--reflectionoracle"></a><span data-ttu-id="99049-112">targetStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="99049-112">targetStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="99049-113">Um Oracle que reflete o estado final desejado.</span><span class="sxs-lookup"><span data-stu-id="99049-113">An oracle that reflects about the desired final state.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="99049-114">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="99049-114">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="99049-115">Um registro para executar amplificação de amplitude em.</span><span class="sxs-lookup"><span data-stu-id="99049-115">A register to perform amplitude amplification on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="99049-116">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="99049-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

