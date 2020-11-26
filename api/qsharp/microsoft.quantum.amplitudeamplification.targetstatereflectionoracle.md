---
uid: Microsoft.Quantum.AmplitudeAmplification.TargetStateReflectionOracle
title: Função TargetStateReflectionOracle
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: TargetStateReflectionOracle
qsharp.summary: >-
  Constructs a `ReflectionOracle` about the target state uniquely marked by the flag qubit.

  The target state has a single qubit set to 1, and all others 0: $\ket{1}_f$.
ms.openlocfilehash: 65ad316a6ac986ebd0dc28b25859026a60aa3239
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191101"
---
# <a name="targetstatereflectionoracle-function"></a>Função TargetStateReflectionOracle

Namespace: [Microsoft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Constrói um `ReflectionOracle` sobre o estado de destino exclusivamente marcado pelo sinalizador qubit.

O estado de destino tem um único qubit definido como 1 e todos os outros 0: $ \ket {1} _F $.

```qsharp
function TargetStateReflectionOracle (idxFlagQubit : Int) : Microsoft.Quantum.Oracles.ReflectionOracle
```


## <a name="input"></a>Entrada

### <a name="idxflagqubit--int"></a>idxFlagQubit: [int](xref:microsoft.quantum.lang-ref.int)

Index para sinalizar qubit $f $ do Oracle.



## <a name="output--reflectionoracle"></a>Saída: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

Um `ReflectionOracle` que reflete o estado marcado por $ \ket {1} _F $.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ReflectionOracle](xref:Microsoft.Quantum.Canon.ReflectionOracle)