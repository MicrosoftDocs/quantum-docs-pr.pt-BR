---
uid: Microsoft.Quantum.Characterization.ContinuousPhaseEstimationIteration
title: Operação ContinuousPhaseEstimationIteration
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: ContinuousPhaseEstimationIteration
qsharp.summary: Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using arbitrary real powers of a unitary oracle.
ms.openlocfilehash: 3c0f6cf084311598346b25dd7028e290946cd87f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216278"
---
# <a name="continuousphaseestimationiteration-operation"></a>Operação ContinuousPhaseEstimationIteration

Namespace: [Microsoft. Quantum. caracterization](xref:Microsoft.Quantum.Characterization)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Executa uma única iteração de um algoritmo de estimativa de fase iterativa (controlado de forma clássica) usando potências reais arbitrárias de um Oracle unitário.

```qsharp
operation ContinuousPhaseEstimationIteration (oracle : Microsoft.Quantum.Oracles.ContinuousOracle, time : Double, theta : Double, targetState : Qubit[], controlQubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="oracle--continuousoracle"></a>Oracle: [ContinuousOracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)

Operação agindo em um Double $t $ e um registro, de modo que $U ^ t $ seja aplicado ao registro fornecido, em que $U $ é o unitário cuja fase deve ser estimada e onde $t $ é o número inteiro de energia concedido ao Oracle


### <a name="time--double"></a>hora: [duplo](xref:microsoft.quantum.lang-ref.double)

Número de vezes para aplicar o Oracle unitário fornecido.


### <a name="theta--double"></a>teta: [duplo](xref:microsoft.quantum.lang-ref.double)

Ângulo pelo qual inverter a fase no qubit de controle antes de agir no estado de destino.


### <a name="targetstate--qubit"></a>TargetState: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Registro de estado acionado pelo Oracle unitário determinado.


### <a name="controlqubit--qubit"></a>controlQubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)





## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

