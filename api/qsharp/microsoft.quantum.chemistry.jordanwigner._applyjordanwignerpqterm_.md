---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ApplyJordanWignerPQTerm_
title: Operação _ApplyJordanWignerPQTerm_
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ApplyJordanWignerPQTerm_
qsharp.summary: Applies time-evolution by a PQ term described by a `GeneratorIndex`.
ms.openlocfilehash: ef9ed8a9361548730d716cf0fea8ff08c82b6f59
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96215904"
---
# <a name="_applyjordanwignerpqterm_-operation"></a>Operação _ApplyJordanWignerPQTerm_

Namespace: [Microsoft. Quantum. química. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Pacote: [Microsoft. Quantum. química](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Aplica a evolução de tempo por um termo de PQ descrito por um `GeneratorIndex` .

```qsharp
operation _ApplyJordanWignerPQTerm_ (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, extraParityQubits : Qubit[], qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="term--generatorindex"></a>termo: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

`GeneratorIndex` representando um termo de PQ.


### <a name="stepsize--double"></a>Etapas: [duplo](xref:microsoft.quantum.lang-ref.double)

Duração da evolução do tempo.


### <a name="extraparityqubits--qubit"></a>extraParityQubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Qubits de paridade opcionais que invertem o sinal de tempo-evolução.


### <a name="qubits--qubit"></a>qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Qubits Hamiltonian.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

