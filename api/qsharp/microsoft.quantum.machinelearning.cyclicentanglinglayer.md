---
uid: Microsoft.Quantum.MachineLearning.CyclicEntanglingLayer
title: Função CyclicEntanglingLayer
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: CyclicEntanglingLayer
qsharp.summary: Returns an array of singly controlled rotations along a given axis, arranged cyclically across a register of qubits, and parameterized by distinct model parameters.
ms.openlocfilehash: 5d0af0a60217b69dc7eb8ece8952f2a7f0c09280
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847377"
---
# <a name="cyclicentanglinglayer-function"></a>Função CyclicEntanglingLayer

Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Retorna uma matriz de rotações controladas isoladamente ao longo de um determinado eixo, organizadas de forma cíclica em um registro de qubits e parametrizadas por parâmetros de modelo distintos.

```qsharp
function CyclicEntanglingLayer (nQubits : Int, axis : Pauli, stride : Int) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a>Entrada

### <a name="nqubits--int"></a>nQubits: [int](xref:microsoft.quantum.lang-ref.int)

O número de qubits acionadas pela camada determinada.


### <a name="axis--pauli"></a>eixo: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

O eixo de rotação para cada rotação na camada especificada.


### <a name="stride--int"></a>Stride: [int](xref:microsoft.quantum.lang-ref.int)

A separação entre os índices de destino e de controle para cada rotação.



## <a name="output--controlledrotation"></a>Saída: [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]

Uma matriz de rotações controladas de dois qubits, projetadas de forma cíclica em um registro de `nQubits` qubits.

## <a name="example"></a>Exemplo

Os itens a seguir são equivalentes:

```qsharp
let layer = CyclicEntanglingLayer(3, PauliX, 2);
let layer = [
    ControlledRotation((0, [2]), PauliX, 0),
    ControlledRotation((1, [0]), PauliX, 1),
    ControlledRotation((2, [1]), PauliX, 2)
];
```