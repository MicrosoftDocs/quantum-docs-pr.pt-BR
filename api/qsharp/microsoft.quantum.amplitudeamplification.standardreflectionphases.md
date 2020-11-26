---
uid: Microsoft.Quantum.AmplitudeAmplification.StandardReflectionPhases
title: Função StandardReflectionPhases
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: StandardReflectionPhases
qsharp.summary: Computes partial reflection phases for standard amplitude amplification.
ms.openlocfilehash: 316c8f22a16859ebb439824eda9a5aa02c750b5d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191118"
---
# <a name="standardreflectionphases-function"></a>Função StandardReflectionPhases

Namespace: [Microsoft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Computa fases de reflexo parcial para amplificação de amplitude padrão.

```qsharp
function StandardReflectionPhases (nIterations : Int) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a>Entrada

### <a name="niterations--int"></a>nIterations: [int](xref:microsoft.quantum.lang-ref.int)

Número de iterações de amplificação de amplitude para as quais gerar fases de reflexo parcial.



## <a name="output--reflectionphases"></a>Saída: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

Uma operação que implementa as fases especificadas como reflexos parciais

## <a name="remarks"></a>Comentários

Todas as fases são $ \pi $, exceto a primeira reflexão sobre o estado de início e a última reflexão sobre o estado de destino, que são $0 $.