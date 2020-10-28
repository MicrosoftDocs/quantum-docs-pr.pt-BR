---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhasesAsReflectionPhases
title: Função RotationPhasesAsReflectionPhases
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhasesAsReflectionPhases
qsharp.summary: Converts phases specified as single-qubit rotations to phases specified as partial reflections.
ms.openlocfilehash: d62a7584324c9467ccc759e4bed81acbceee719c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694889"
---
# <a name="rotationphasesasreflectionphases-function"></a>Função RotationPhasesAsReflectionPhases

Namespace: [Microsoft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

Agrupa [](https://nuget.org/packages/)


Converte as fases especificadas como rotações de qubit único para fases especificadas como reflexos parciais.

```qsharp
function RotationPhasesAsReflectionPhases (rotPhases : Microsoft.Quantum.AmplitudeAmplification.RotationPhases) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a>Entrada

### <a name="rotphases--rotationphases"></a>rotPhases: [RotationPhases](xref:Microsoft.Quantum.AmplitudeAmplification.RotationPhases)

Matriz de rotações de qubit único a serem convertidas em reflexões parciais.



## <a name="output--reflectionphases"></a>Saída: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

Uma operação que implementa as fases especificadas como reflexos parciais.

## <a name="references"></a>Referências

Usamos a Convenção em

- [ *G.H. Low, I. L. Chuang*](https://arxiv.org/abs/1707.05391) para relacionar fases de rotação de qubit único a fases do operador de reflexão.