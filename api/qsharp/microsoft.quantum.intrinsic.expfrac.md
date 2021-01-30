---
uid: Microsoft.Quantum.Intrinsic.ExpFrac
title: Operação ExpFrac
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: ExpFrac
qsharp.summary: >-
  Applies the exponential of a multi-qubit Pauli operator with an argument given by a dyadic fraction.

  \begin{align} e^{i \pi k [P_0 \otimes P_1 \cdots P_{N-1}] / 2^n}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.
ms.openlocfilehash: 6634caff164c841876fb53e79c3f93254a7d624c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849428"
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

