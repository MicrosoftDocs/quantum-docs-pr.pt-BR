---
uid: Microsoft.Quantum.Intrinsic.Measure
title: Operação de medida
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Measure
qsharp.summary: >-
  Performs a joint measurement of one or more qubits in the specified Pauli bases.

  The output result is given by the distribution: \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \frac12 \braket{ \psi \mid| \left( \boldone + P_0 \otimes P_1 \otimes \cdots \otimes P_{N-1} \right) \mid| \psi }, \end{align} where $P_i$ is the $i$th element of `bases`, and where $N = \texttt{Length}(\texttt{bases})$. That is, measurement returns a `Result` $d$ such that the eigenvalue of the observed measurement effect is $(-1)^d$.
ms.openlocfilehash: bf0a606b1bfc8c4762245422450ec26907ec1946
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98818777"
---
# <a name="measure-operation"></a>Operação de medida

Namespace: [Microsoft. Quantum. intrínseco](xref:Microsoft.Quantum.Intrinsic)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Executa uma medida conjunta de um ou mais qubits nas bases de Pauli especificadas.

O resultado de saída é fornecido pela distribuição: \begin{align} \Pr (\texttt{Zero} | \ket{\psi}) = \frac12 \braket{\psi \mid | \left (\boldone + P_0 \otimes P_1 \otimes \cdots \otimes P_ {N-1} \right) \mid | \psi}, \end{align} em que $P _i $ é o elemento $i $ th de `bases` e onde $N = \texttt{Length} (\texttt{bases}) $.
Ou seja, a medida retorna um `Result` $d $ de modo que o eigenvalue do efeito de medição observado é $ (-1) ^ d $.

```qsharp
operation Measure (bases : Pauli[], qubits : Qubit[]) : Result
```


## <a name="input"></a>Entrada

### <a name="bases--pauli"></a>bases: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Matriz de valores de Pauli de qubit único que indicam os fatores de produto tensor em cada qubit.


### <a name="qubits--qubit"></a>qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Registro de qubits a ser medido.



## <a name="output--__invalidresult__"></a>Saída: __inválida <Result>__

`Zero` Se o $ + $1 eigenvalue for observado e `One` se o eigenvalue $-$1 for observado.

## <a name="remarks"></a>Comentários

Se a matriz de base e a matriz qubit tiverem comprimentos diferentes, a operação falhará.