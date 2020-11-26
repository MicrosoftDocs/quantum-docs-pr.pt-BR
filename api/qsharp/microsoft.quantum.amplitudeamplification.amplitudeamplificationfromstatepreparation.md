---
uid: Microsoft.Quantum.AmplitudeAmplification.AmplitudeAmplificationFromStatePreparation
title: Função AmplitudeAmplificationFromStatePreparation
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: AmplitudeAmplificationFromStatePreparation
qsharp.summary: Amplitude amplification by oracles for partial reflections.
ms.openlocfilehash: 30e1cf6e353b8a4491e13a9e2f588ec9cc103cb4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191594"
---
# <a name="amplitudeamplificationfromstatepreparation-function"></a>Função AmplitudeAmplificationFromStatePreparation

Namespace: [Microsoft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Amplificação de amplitude por Oracle para reflexões parciais.

```qsharp
function AmplitudeAmplificationFromStatePreparation (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, stateOracle : Microsoft.Quantum.Oracles.StateOracle, idxFlagQubit : Int) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a>Entrada

### <a name="phases--reflectionphases"></a>fases: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

Fases de reflexos parciais


### <a name="stateoracle--stateoracle"></a>stateOracle: [stateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)

O Oracle $A $ unitário que prepara o estado de início


### <a name="idxflagqubit--int"></a>idxFlagQubit: [int](xref:microsoft.quantum.lang-ref.int)

Índice para sinalizar qubit



## <a name="output--qubit--unit--is-adj--ctl"></a>Saída: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL

Uma operação que implementa amplificação de amplitude por Oracle que são implementadas por reflexões parciais.

## <a name="remarks"></a>Comentários

Isso impõe condições mais estritas na forma dos Estados inicial e de destino do que em `AmpAmpByReflectionPhases` .
Supõe-se que o estado de destino seja marcado por $ \ket {1} \_ f $.
Presume-se que \begin{align} A\ket {0} \_ {f} \ket {0} \_ s = \lambda\ket {1} \_ f\ket {\ Text {Target}} \_ s + \sqrt{1-| \lambda | ^ 2} \ket {0} \_ f\cdots, \end{align} na maioria dos casos `flagQubit` e `auxiliaryRegister` sejam inicializados no estado $ \ket {0} \_ {f} \ket {0} \_ s $.