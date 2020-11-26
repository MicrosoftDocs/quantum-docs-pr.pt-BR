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
# <a name="applyamplitudeamplification-operation"></a>Operação ApplyAmplitudeAmplification

Namespace: [Microsoft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica amplificação de amplitude em um determinado registro, usando um determinado conjunto de fases e ORACLES para refletir sobre os Estados inicial e final.

```qsharp
operation ApplyAmplitudeAmplification (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, targetStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, target : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="phases--reflectionphases"></a>fases: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

Um conjunto de fases que descreve os reflexos parciais em cada etapa do algoritmo de amplificação de amplitude. Para ver um exemplo, consulte @"microsoft.quantum.amplitudeamplification.standardreflectionphases".


### <a name="startstatereflection--reflectionoracle"></a>startStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

Um Oracle que reflete o estado inicial.


### <a name="targetstatereflection--reflectionoracle"></a>targetStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

Um Oracle que reflete o estado final desejado.


### <a name="target--qubit"></a>destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Um registro para executar amplificação de amplitude em.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

