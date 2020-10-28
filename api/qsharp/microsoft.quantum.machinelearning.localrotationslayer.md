---
uid: Microsoft.Quantum.MachineLearning.LocalRotationsLayer
title: Função LocalRotationsLayer
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: LocalRotationsLayer
qsharp.summary: Returns an array of uncontrolled (single-qubit) rotations along a given axis, with one rotation for each qubit in a register, parameterized by distinct model parameters.
ms.openlocfilehash: 8a3557f76d5d7a7b6375e5640cf6d11172cd38a6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696804"
---
# <a name="localrotationslayer-function"></a>Função LocalRotationsLayer

Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Agrupa [](https://nuget.org/packages/)


Retorna uma matriz de rotações não controladas (de qubit único) ao longo de um determinado eixo, com uma rotação para cada qubit em um registro, parametrizada por parâmetros de modelo distintos.

```qsharp
function LocalRotationsLayer (nQubits : Int, axis : Pauli) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a>Entrada

### <a name="nqubits--int"></a>nQubits: [int](xref:microsoft.quantum.lang-ref.int)

O número de qubits acionadas pela camada determinada.


### <a name="axis--pauli"></a>eixo: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

O eixo de rotação para cada rotação na camada especificada.



## <a name="output--controlledrotation"></a>Saída: [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]

Uma matriz de rotações controladas sobre o eixo determinado, uma em cada `nQubits` qubits.