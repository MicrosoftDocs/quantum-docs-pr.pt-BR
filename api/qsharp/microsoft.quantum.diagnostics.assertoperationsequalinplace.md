---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlace
title: Operação AssertOperationsEqualInPlace
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualInPlace
qsharp.summary: >-
  Given two operations, asserts that they act identically for all input states.

  This assertion is implemented by checking the action of the operations on all states of the form $V_0 \otimes ... \otimes V_{n-1}$, where $V_k$ is one of the states $\ket{0}$, $\ket{1}$, $\ket{+}$ and $\ket{i}$ (+1 eigenstate of Pauli Y operator).

  This assertion uses $n$ qubits and requires multiple calls of the operations being compared.
ms.openlocfilehash: 9b17bac9d95baf5a542604892c64130bf35d7f69
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202423"
---
# <a name="assertoperationsequalinplace-operation"></a>Operação AssertOperationsEqualInPlace

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Dadas duas operações, afirma que elas agem de forma idêntica para todos os Estados de entrada.

Essa asserção é implementada verificando a ação das operações em todos os Estados do formulário $V _0 \otimes... \otimes V_ {n-1} $, em que $V _k $ é um dos Estados $ \ket {0} $, $ \ket {1} $, $ \ket{+} $ e $ \ket{i} $ (+ 1 eigenstate do operador Y Pauli).

Essa declaração usa $n $ qubits e requer que várias chamadas das operações sejam comparadas.

```qsharp
operation AssertOperationsEqualInPlace (nQubits : Int, givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a>Entrada

### <a name="nqubits--int"></a>nQubits: [int](xref:microsoft.quantum.lang-ref.int)

O número de qubits $n $ em que as `givenU` operações `expectedU` funcionam.


### <a name="givenu--qubit--unit"></a>dada: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit) de> 

Operação em $n $ qubits a ser verificada.


### <a name="expectedu--qubit--unit--is-adj"></a>expectedd: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj

Operação de referência em $n $ qubits que deve `givenU` ser comparada.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Referências

A base dos Estados $ \ket {0} $, $ \ket {1} $, $ \ket{+} $ e $ \ket{i} $ é a base Chuang-Nielsen, descrita em [ *i. L. Chuang, M. A. Nielsen*](https://arxiv.org/abs/quant-ph/9610001).

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Diagnostics. AssertOperationsEqualReferenced](xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced)