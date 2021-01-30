---
uid: Microsoft.Quantum.Arithmetic.AssertProbInt
title: Operação AssertProbInt
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertProbInt
qsharp.summary: Asserts that the probability of a specific state of a quantum register has the expected value.
ms.openlocfilehash: 85ff04bbad9dc2ed0f803db65508fdfbb0d22c56
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843399"
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



## <a name="example"></a>Exemplo

Suponha que o `qubits` registro codifica um estado de Quantum de 3 qubit $ \ket{\psi} = \ sqrt {1/8} \ ket {0} + \ sqrt {7/8} \ ket {6} $ no formato little-endian.
Isso significa que o número afirma $ \ket {0} \equiv\ket {0} \ket {0} \ket {0} $ e $ \ket {6} \equiv\ket \ket \ket {0} {1} {1} $. Em seguida, as seguintes declarações serão realizadas com sucesso:

```qsharp
AssertProbInt(0, 0.125, qubits, 10e-10);
AssertProbInt(6, 0.875, qubits, 10e-10);
```