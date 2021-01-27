---
uid: Microsoft.Quantum.AmplitudeAmplification.ObliviousAmplitudeAmplificationFromStatePreparation
title: Função ObliviousAmplitudeAmplificationFromStatePreparation
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ObliviousAmplitudeAmplificationFromStatePreparation
qsharp.summary: Oblivious amplitude amplification by oracles for partial reflections.
ms.openlocfilehash: 873c436d4b8d8efc9dc61c2baba9b0e0f7f09fc2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845818"
---
# <a name="obliviousamplitudeamplificationfromstatepreparation-function"></a>Função ObliviousAmplitudeAmplificationFromStatePreparation

Namespace: [Microsoft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Amplificação de amplitude de alheios por Oracle para reflexões parciais.

```qsharp
function ObliviousAmplitudeAmplificationFromStatePreparation (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle, idxFlagQubit : Int) : ((Qubit[], Qubit[]) => Unit is Adj + Ctl)
```


## <a name="input"></a>Entrada

### <a name="phases--reflectionphases"></a>fases: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

Fases de reflexos parciais


### <a name="startstateoracle--deterministicstateoracle"></a>startStateOracle: [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)

O Oracle $A $ unitário que prepara o estado de início auxiliar


### <a name="signaloracle--obliviousoracle"></a>signalOracle: [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)

O $O do Oracle unitário $ do tipo `ObliviousOracle` que atua em conjunto no registro auxiliar e do sistema


### <a name="idxflagqubit--int"></a>idxFlagQubit: [int](xref:microsoft.quantum.lang-ref.int)

Índice para registro de sinalizador de qubit único



## <a name="output--qubitqubit--unit--is-adj--ctl"></a>Saída: ([qubit](xref:microsoft.quantum.lang-ref.qubit)[],[qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL

Uma operação que implementa a amplificação de amplitude de alheios com base em reflexos parciais.

## <a name="remarks"></a>Comentários

Isso impõe condições mais estritas na forma de inicialização auxiliar e Estados de destino do que em `AmpAmpObliviousByReflectionPhases` .
Supõe-se que $A \ket {0} \_ f\ket {0} \_ a = \ket{\Text{Start}} \_ {FA} $ prepara o estado de início auxiliar $ \ket{\Text{Start}} \_ {FA} $ da base computacional $ \ket {0} \_ f\ket {0} $.
Supõe-se que o estado de destino seja marcado por $ \ket {1} \_ f $.
Supõe-se que \begin{align} O\ket {\ Text {Start}} \_ {FA} \ket{\psi} \_ s = \lambda\ket {1} \_ f\ket {\ Text {qualquer coisa}} \_ a\ket {\ Text {Target}} \_ s U \ket{\psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket {0} \_ f\cdots, \end{align} para alguns $U unitários $.