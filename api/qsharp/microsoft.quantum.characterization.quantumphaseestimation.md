---
uid: Microsoft.Quantum.Characterization.QuantumPhaseEstimation
title: Operação QuantumPhaseEstimation
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: QuantumPhaseEstimation
qsharp.summary: Performs the quantum phase estimation algorithm for a given oracle `U` and `targetState`, reading the phase into a big-endian quantum register.
ms.openlocfilehash: 14ba3e012f6561e7089f9fe59b2a13516b211d51
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204208"
---
# <a name="quantumphaseestimation-operation"></a>Operação QuantumPhaseEstimation

Namespace: [Microsoft. Quantum. caracterization](xref:Microsoft.Quantum.Characterization)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Executa o algoritmo de estimativa de fase Quantum para um determinado Oracle `U` e `targetState` , em seguida, lendo a fase em um registro de Quantum big-endian.

```qsharp
operation QuantumPhaseEstimation (oracle : Microsoft.Quantum.Oracles.DiscreteOracle, targetState : Qubit[], controlRegister : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="oracle--discreteoracle"></a>Oracle: [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)

Uma operação que implementa $U ^ m $ para o número inteiro é m.


### <a name="targetstate--qubit"></a>TargetState: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Um registro da Quantum que representa o estado $ \ket{\phi} $ foi acionado por $U $. Se $ \ket{\phi} $ for um eigenstate de $U $, $U \ket{\phi} = e ^ {i\phi} \ket{\phi} $ para $ \phi na [0, 2 \ PI) $ uma fase desconhecida.


### <a name="controlregister--bigendian"></a>controlRegister: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)

Um registro inteiro de representação big endian que pode ser usado para controlar o Oracle fornecido e que conterá uma representação de $ \phi $ seguindo o aplicativo desta operação. O controlRegister é considerado para iniciar no estado inicial $ \ket{00\cdots 0} $, em que o comprimento do Registro indica a precisão desejada.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

