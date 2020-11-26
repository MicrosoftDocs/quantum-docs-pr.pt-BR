---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyFixedPointAmplification
title: Operação ApplyFixedPointAmplification
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyFixedPointAmplification
qsharp.summary: Fixed-Point Amplitude Amplification algorithm
ms.openlocfilehash: 13e70b1ebd5e3bf0996e6a76f4bffe57ca2d2250
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191526"
---
# <a name="applyfixedpointamplification-operation"></a>Operação ApplyFixedPointAmplification

Namespace: [Microsoft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Algoritmo de amplificação Fixed-Point amplitude

```qsharp
operation ApplyFixedPointAmplification (statePrepOracle : Microsoft.Quantum.Oracles.StateOracle, startQubits : Qubit[]) : Unit
```


## <a name="input"></a>Entrada

### <a name="statepreporacle--stateoracle"></a>statePrepOracle: [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)

A Oracle unitário que prepara o estado de início.


### <a name="startqubits--qubit"></a>startQubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Registro de qubit



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

O startQubits deve estar no estado $ \ket{0 \cdots 0} $. Esta operação itera em várias consultas em potências de $2 $ até que um número máximo de consultas seja atingido ou o estado de destino seja encontrado.