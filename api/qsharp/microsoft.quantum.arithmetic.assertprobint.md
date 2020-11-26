---
uid: Microsoft.Quantum.Arithmetic.AssertProbInt
title: Operação AssertProbInt
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertProbInt
qsharp.summary: Asserts that the probability of a specific state of a quantum register has the expected value.
ms.openlocfilehash: b95c2c6294dd5a95b7215c22bd6c50a41635f432
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223690"
---
# <a name="assertprobint-operation"></a>Operação AssertProbInt

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Declara que a probabilidade de um estado específico de um registro Quantum tem o valor esperado.

```qsharp
operation AssertProbInt (stateIndex : Int, expected : Double, qubits : Microsoft.Quantum.Arithmetic.LittleEndian, tolerance : Double) : Unit
```


## <a name="description"></a>Descrição

Dado um estado $n $-qubit Quantum $ \ket{\psi} = \sum ^ {2 ^ n-1} _ {j = 0} \ alpha_j \ket{j} $, declara que a probabilidade $ | \ alpha_j | ^ 2 $ do estado $ \ket{j} $ indexado por $j $ tem o valor esperado.

## <a name="input"></a>Entrada

### <a name="stateindex--int"></a>stateIndex: [int](xref:microsoft.quantum.lang-ref.int)

O índice $j $ do estado $ \ket{j} $ representado por um `LittleEndian` registro.


### <a name="expected--double"></a>esperado: [duplo](xref:microsoft.quantum.lang-ref.double)

O valor esperado de $ | \ alpha_j | ^ 2 $.


### <a name="qubits--littleendian"></a>qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

O registro qubit que armazena $ \ket{\psi} $ no formato little-endian.


### <a name="tolerance--double"></a>tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)

Tolerância absoluta na diferença entre real e esperado.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

