---
uid: Microsoft.Quantum.Characterization.DiscretePhaseEstimationIteration
title: Operação DiscretePhaseEstimationIteration
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: DiscretePhaseEstimationIteration
qsharp.summary: Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using integer powers of a unitary oracle.
ms.openlocfilehash: 03e2300dcc2d2cb42992e074833c8cd2530e898b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839969"
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

