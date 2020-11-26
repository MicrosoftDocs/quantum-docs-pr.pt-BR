---
uid: Microsoft.Quantum.Intrinsic.CNOT
title: Operação CNOT
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: CNOT
qsharp.summary: >-
  Applies the controlled-NOT (CNOT) gate to a pair of qubits.

  \begin{align} \operatorname{CNOT} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{bmatrix}, \end{align}

  where rows and columns are ordered as in the quantum concepts guide.
ms.openlocfilehash: 90e84f7d0ea7373498632474dfafa23335f0c78e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198967"
---
# <a name="cnot-operation"></a>Operação CNOT

Namespace: [Microsoft. Quantum. intrínseco](xref:Microsoft.Quantum.Intrinsic)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Aplica o portão-NOT (CNOT) controlado a um par de qubits.

\begin{align} \operatorname{CNOT} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \\ \\ 0 & 0 & 1 & 0 \end{bmatrix}, \end{align}

onde as linhas e colunas são ordenadas como no guia de conceitos do Quantum.

```qsharp
operation CNOT (control : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="control--qubit"></a>controle: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Controle qubit para o portão CNOT.


### <a name="target--qubit"></a>destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit de destino para o portão CNOT.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

Equivalente a:

```qsharp
Controlled X([control], target);
```