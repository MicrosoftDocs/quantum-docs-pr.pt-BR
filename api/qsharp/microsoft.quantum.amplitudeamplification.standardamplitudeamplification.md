---
uid: Microsoft.Quantum.AmplitudeAmplification.StandardAmplitudeAmplification
title: Função StandardAmplitudeAmplification
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: StandardAmplitudeAmplification
qsharp.summary: Standard Amplitude Amplification algorithm
ms.openlocfilehash: 23a2b3dbe5ea404059994167f69e11458c0c22ea
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191169"
---
# <a name="standardamplitudeamplification-function"></a>Função StandardAmplitudeAmplification

Namespace: [Microsoft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Algoritmo de amplificação de amplitude padrão

```qsharp
function StandardAmplitudeAmplification (nIterations : Int, stateOracle : Microsoft.Quantum.Oracles.StateOracle, idxFlagQubit : Int) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a>Entrada

### <a name="niterations--int"></a>nIterations: [int](xref:microsoft.quantum.lang-ref.int)

Número de iterações $n $ da amplificação de amplitude


### <a name="stateoracle--stateoracle"></a>stateOracle: [stateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)

O Oracle $A $ unitário que prepara o estado de início


### <a name="idxflagqubit--int"></a>idxFlagQubit: [int](xref:microsoft.quantum.lang-ref.int)

Índice para sinalizar qubit



## <a name="output--qubit--unit--is-adj--ctl"></a>Saída: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL

Uma operação que implementa o algoritmo Quantum da amplificação de amplitude padrão

## <a name="remarks"></a>Comentários

Este é o algoritmo de amplificação de amplitude padrão obtido por uma opção de fases de reflexão computada, `AmpAmpPhasesStandard` supondo que \Begin{align} A\ket {0} \_ {f} \ket {0} \_ s = \lambda\ket {1} \_ f\ket {\ Text {Target}} \_ s + \sqrt{1-| \lambda | ^ 2} \ket {0} \_ f\cdots, \end{align} esta operação prepara o estado \begin{align} \operatorname{AmpAmpByOracle}\ket {0} \_ {f} \ket {0} \_ s = \sin ((2n + 1) \sin ^ {-1} (\lambda)) \ket {1} \_ f\ket {\ Text {Target}} \_ s + \cdots\ket {0} \_ f \end{align} na maioria dos casos `flagQubit` e `auxiliaryRegister` é inicializada no estado $ \ket {0} \_ f\ket {0} \_ a $.

## <a name="references"></a>Referências

- [*G. Brassard, P. Hoyer, M. mosca, A. Tapp*](https://arxiv.org/abs/quant-ph/0005055)