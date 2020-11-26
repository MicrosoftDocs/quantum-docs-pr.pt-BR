---
uid: Microsoft.Quantum.Intrinsic.ExpFrac
title: Operação ExpFrac
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: ExpFrac
qsharp.summary: >-
  Applies the exponential of a multi-qubit Pauli operator with an argument given by a dyadic fraction.

  \begin{align} e^{i \pi k [P_0 \otimes P_1 \cdots P_{N-1}] / 2^n}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.
ms.openlocfilehash: 8ccea068dd61aaf8c1ba384969adef5644e8401e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198988"
---
# <a name="expfrac-operation"></a>Operação ExpFrac

Namespace: [Microsoft. Quantum. intrínseco](xref:Microsoft.Quantum.Intrinsic)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Aplica o exponencial de um operador qubit Pauli com um argumento fornecido por uma fração dyadic.

\begin{align} e ^ {i \pi k [P_0 \otimes P_1 \cdots P_ {N-1}]/2 ^ N}, \end{align} em que $P _i $ é o elemento $i $ th de `paulis` e onde $N = $ `Length(paulis)` .

```qsharp
operation ExpFrac (paulis : Pauli[], numerator : Int, power : Int, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="paulis--pauli"></a>Paulis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Matriz de valores de Pauli de qubit único que indicam os fatores de produto tensor em cada qubit.


### <a name="numerator--int"></a>numerador: [int](xref:microsoft.quantum.lang-ref.int)

O numerador ($k $) na representação de fração dyadic do ângulo pelo qual o registro qubit deve ser girado.


### <a name="power--int"></a>potência: [int](xref:microsoft.quantum.lang-ref.int)

Potência de dois ($n $) especificando o denominador do ângulo pelo qual o registro de qubit deve ser girado.


### <a name="qubits--qubit"></a>qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Registre-se para aplicar a rotação fornecida ao.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

