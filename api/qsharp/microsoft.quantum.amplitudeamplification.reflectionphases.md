---
uid: Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
title: Tipo definido pelo usuário ReflectionPhases
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ReflectionPhases
qsharp.summary: Phases for a sequence of partial reflections in amplitude amplification.
ms.openlocfilehash: 743ece778239c223573a3a8536ae8059cea09d5f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191339"
---
# <a name="reflectionphases-user-defined-type"></a>Tipo definido pelo usuário ReflectionPhases

Namespace: [Microsoft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Fases para uma sequência de reflexos parciais na amplificação de amplitude.

```qsharp

newtype ReflectionPhases = (AboutStart : Double[], AboutTarget : Double[]);
```



## <a name="named-items"></a>Itens nomeados

### <a name="aboutstart--double"></a>AboutStart: [Double](xref:microsoft.quantum.lang-ref.double)[]

Uma matriz de fases para reflexão sobre o estado de início.
### <a name="abouttarget--double"></a>AboutTarget: [Double](xref:microsoft.quantum.lang-ref.double)[]

Uma matriz de fases para reflexão sobre o estado de destino.

## <a name="remarks"></a>Comentários

Ambas as matrizes devem ter comprimento igual. Observe que em muitos casos, a primeira fase sobre o estado de início e a última fase sobre o estado de destino apresenta uma mudança de fase global e pode ser definida como $0 $.