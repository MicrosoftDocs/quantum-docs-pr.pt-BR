---
uid: Microsoft.Quantum.MachineLearning.ControlledRotation
title: Tipo definido pelo usuário ControlledRotation
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ControlledRotation
qsharp.summary: Describes a controlled rotation in terms of its target and control indices, rotation axis, and index into a model parameter vector.
ms.openlocfilehash: afc425c16ab550fd414e656484c9ff6f0f8f3ef4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693321"
---
# <a name="controlledrotation-user-defined-type"></a>Tipo definido pelo usuário ControlledRotation

Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Agrupa [](https://nuget.org/packages/)


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

## <a name="remarks"></a>Comentários

Uma rotação não controlada pode ser representada pela configuração `ControlIndices` para uma matriz vazia de índices, `new Int[0]` .