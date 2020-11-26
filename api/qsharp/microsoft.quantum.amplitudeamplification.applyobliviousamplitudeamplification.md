---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyObliviousAmplitudeAmplification
title: Operação ApplyObliviousAmplitudeAmplification
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyObliviousAmplitudeAmplification
qsharp.summary: Oblivious amplitude amplification by specifying partial reflections.
ms.openlocfilehash: 9b0060201bcdae02a207362a753a0a403cdbb896
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191509"
---
# <a name="applyobliviousamplitudeamplification-operation"></a>Operação ApplyObliviousAmplitudeAmplification

Namespace: [Microsoft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Amplificação de amplitude de alheios especificando reflexões parciais.

```qsharp
operation ApplyObliviousAmplitudeAmplification (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, targetStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle, auxiliaryRegister : Qubit[], systemRegister : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="phases--reflectionphases"></a>fases: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

Fases de reflexos parciais


### <a name="startstatereflection--reflectionoracle"></a>startStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

Operador de reflexo sobre o estado de início do registro auxiliar


### <a name="targetstatereflection--reflectionoracle"></a>targetStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

Operador de reflexão sobre o estado de destino do registro auxiliar


### <a name="signaloracle--obliviousoracle"></a>signalOracle: [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)

O $O do Oracle unitário $ do tipo `ObliviousOracle` que atua em conjunto nos registros auxiliares e do sistema.


### <a name="auxiliaryregister--qubit"></a>auxiliaryRegister: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Registro auxiliar


### <a name="systemregister--qubit"></a>systemRegister: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Registro do sistema



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

Dado um estado de início auxiliar específico $ \ket{\Text{Start}} \_ a $, um estado de destino auxiliar específico $ \ket{\Text{Target}} \_ a $ e qualquer estado do sistema $ \ket{\psi} \_ s $, suponha que \begin{align} O\ket {\ Text {Start}} \_ a\ket {\ psi} \_ s = \lambda\ket{\Text{Target}} \_ a U \ket{\psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket{\text{target} ^ \perp} \_ a\cdots \end{align} para alguns $U unitários $.
Por uma sequência de reflexos sobre os Estados de início e de destino no registro auxiliar intercalado por aplicativos do `signalOracle` e seu adjacente, a probabilidade de êxito da aplicação de U pode ser alterada.

Na maioria dos casos, `auxiliaryRegister` é inicializado no estado $ \ket{\Text{Start}} \_ a $.

## <a name="references"></a>Referências

Consulte

- [ *D.W. Berry, am Childs, r. Cleve, r. Kothari, R.D. Somma*](https://arxiv.org/abs/1312.1414) para a versão padrão.
  Consulte
- [ *G.H. Low, I.L. Chuang*](https://arxiv.org/abs/1610.06546) para uma generalização até reflexões parciais.