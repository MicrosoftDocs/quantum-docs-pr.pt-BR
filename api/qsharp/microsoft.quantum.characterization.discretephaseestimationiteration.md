---
uid: Microsoft.Quantum.Characterization.DiscretePhaseEstimationIteration
title: Operação DiscretePhaseEstimationIteration
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: DiscretePhaseEstimationIteration
qsharp.summary: Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using integer powers of a unitary oracle.
ms.openlocfilehash: 8ce1e1a2bda6507285f055c87619a8760c891082
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204378"
---
# <a name="discretephaseestimationiteration-operation"></a>Operação DiscretePhaseEstimationIteration

Namespace: [Microsoft. Quantum. caracterization](xref:Microsoft.Quantum.Characterization)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Executa uma única iteração de um algoritmo de estimativa de fase iterativa (controlado de forma clássica) usando potências de inteiros de um Oracle unitário.

```qsharp
operation DiscretePhaseEstimationIteration (oracle : Microsoft.Quantum.Oracles.DiscreteOracle, power : Int, theta : Double, targetState : Qubit[], controlQubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="oracle--discreteoracle"></a>Oracle: [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)

Operação que atua em um inteiro e um registro, de modo que $U ^ m $ seja aplicada ao registro fornecido, em que $U $ é o unitário cuja fase deve ser estimada e onde $m $ é o número inteiro de energia fornecido para o Oracle


### <a name="power--int"></a>potência: [int](xref:microsoft.quantum.lang-ref.int)

Número de vezes para aplicar o Oracle unitário fornecido.


### <a name="theta--double"></a>teta: [duplo](xref:microsoft.quantum.lang-ref.double)

Ângulo pelo qual inverter a fase no qubit de controle antes de agir no estado de destino.


### <a name="targetstate--qubit"></a>TargetState: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Registro de estado acionado pelo Oracle unitário determinado.


### <a name="controlqubit--qubit"></a>controlQubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Um qubit auxiliar usado para controlar o aplicativo do Oracle fornecido.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

