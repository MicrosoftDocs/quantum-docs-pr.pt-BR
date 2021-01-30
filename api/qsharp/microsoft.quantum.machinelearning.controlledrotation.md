---
uid: Microsoft.Quantum.MachineLearning.ControlledRotation
title: Tipo definido pelo usuário ControlledRotation
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ControlledRotation
qsharp.summary: Describes a controlled rotation in terms of its target and control indices, rotation axis, and index into a model parameter vector.
ms.openlocfilehash: 231afe65da3640218cbc97b9d49eae21bf6e1786
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847404"
---
# <a name="controlledrotation-user-defined-type"></a>Tipo definido pelo usuário ControlledRotation

Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Descreve uma rotação controlada em termos de seus índices de destino e controle, eixo de rotação e índice em um vetor de parâmetro de modelo.

```qsharp

newtype ControlledRotation = ((TargetIndex : Int, ControlIndices : Int[]), Axis : Pauli, ParameterIndex : Int);
```



## <a name="named-items"></a>Itens nomeados

### <a name="targetindex--int"></a>TargetIndex: [int](xref:microsoft.quantum.lang-ref.int)

Índice do qubit de destino para esta rotação controlada.
### <a name="controlindices--int"></a>ControlIndices: [int](xref:microsoft.quantum.lang-ref.int)[]

Uma matriz dos índices de qubit de controle para essa rotação.
### <a name="axis--pauli"></a>Eixo: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

O eixo desta rotação.
### <a name="parameterindex--int"></a>ParameterIndex: [int](xref:microsoft.quantum.lang-ref.int)

Um índice em um vetor de parâmetro de modelo que descreve o ângulo dessa rotação.

## <a name="example"></a>Exemplo

O seguinte representa uma rotação sobre o eixo $X $ do primeiro qubit em um registro, controlado no segundo qubit e com um ângulo fornecido pelo quarto parâmetro em um modelo sequencial:

```qsharp
let controlledRotation = ControlledRotation(
    (0, [1]),
    PauliX,
    3
)
```

## <a name="remarks"></a>Comentários

Uma rotação não controlada pode ser representada pela configuração `ControlIndices` para uma matriz vazia de índices, `new Int[0]` .