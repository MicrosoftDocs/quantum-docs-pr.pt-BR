---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhases
title: Tipo definido pelo usuário RotationPhases
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhases
qsharp.summary: Phases for a sequence of single-qubit rotations in amplitude amplification.
ms.openlocfilehash: 2f955ce3bfb9ea057c26c79547895df39ed322ab
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843959"
---
# <a name="rotationphases-user-defined-type"></a>Tipo definido pelo usuário RotationPhases

Namespace: [Microsoft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Fases para uma sequência de rotações de qubit única na amplificação de amplitude.

```qsharp

newtype RotationPhases = (Double[]);
```



## <a name="remarks"></a>Comentários

O primeiro parâmetro é uma matriz de fases para reflexões, expressa como um produto de rotações de qubit único.
[ G.H. Baixa, I. L Chuang, https://arxiv.org/abs/1707.05391 ].