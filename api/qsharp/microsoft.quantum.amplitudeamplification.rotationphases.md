---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhases
title: Tipo definido pelo usuário RotationPhases
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhases
qsharp.summary: Phases for a sequence of single-qubit rotations in amplitude amplification.
ms.openlocfilehash: b0373f964b77f8ea561c6e96b11e476b42e7fc55
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694891"
---
# <a name="rotationphases-user-defined-type"></a>Tipo definido pelo usuário RotationPhases

Namespace: [Microsoft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

Agrupa [](https://nuget.org/packages/)


Fases para uma sequência de rotações de qubit única na amplificação de amplitude.

```qsharp

newtype RotationPhases = (Double[]);
```



## <a name="remarks"></a>Comentários

O primeiro parâmetro é uma matriz de fases para reflexões, expressa como um produto de rotações de qubit único.
[ G.H. Baixa, I. L Chuang, https://arxiv.org/abs/1707.05391 ].