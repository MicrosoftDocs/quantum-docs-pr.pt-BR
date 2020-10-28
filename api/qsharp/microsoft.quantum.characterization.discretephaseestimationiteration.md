---
uid: Microsoft.Quantum.Characterization.DiscretePhaseEstimationIteration
title: Operação DiscretePhaseEstimationIteration
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: DiscretePhaseEstimationIteration
qsharp.summary: Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using integer powers of a unitary oracle.
ms.openlocfilehash: 167b53d7108c64d11a4f258d17e90ba78d7dd8d8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693851"
---
# <a name="discretephaseestimationiteration-operation"></a>Operação DiscretePhaseEstimationIteration

Namespace: [Microsoft. Quantum. caracterization](xref:Microsoft.Quantum.Characterization)

Agrupa [](https://nuget.org/packages/)


Executa uma única iteração de um algoritmo de estimativa de fase iterativa (controlado de forma clássica) usando potências de inteiros de um Oracle unitário.

```qsharp
operation DiscretePhaseEstimationIteration (oracle : Microsoft.Quantum.Oracles.DiscreteOracle, power : Int, theta : Double, targetState : Qubit[], controlQubit : Qubit) : Unit
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

