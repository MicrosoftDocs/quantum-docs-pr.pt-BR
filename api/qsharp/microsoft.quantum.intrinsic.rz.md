---
uid: Microsoft.Quantum.Intrinsic.Rz
title: Operação RZ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Rz
qsharp.summary: >-
  Applies a rotation about the $z$-axis by a given angle.

  \begin{align} R_z(\theta) \mathrel{:=} e^{-i \theta \sigma_z / 2} = \begin{bmatrix} e^{-i \theta / 2} & 0 \\\\ 0 & e^{i \theta / 2} \end{bmatrix}. \end{align}
ms.openlocfilehash: 4282fcc216173234ec742991b8f0fa1be203da0d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849284"
---
# <a name="rz-operation"></a>Operação RZ

Namespace: [Microsoft. Quantum. intrínseco](xref:Microsoft.Quantum.Intrinsic)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Aplica uma rotação sobre o eixo $ $z por um determinado ângulo.

\begin{align} R_z (\theta) \mathrel{: =} e ^ {-i \theta \ sigma_z/2} = \begin{bmatrix} e ^ {-i \theta/2} & 0 \\ \\ 0 & e ^ {i \theta/2} \end{bmatrix}.
\end{align}

```qsharp
operation Rz (theta : Double, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="theta--double"></a>teta: [duplo](xref:microsoft.quantum.lang-ref.double)

Ângulo sobre o qual o qubit deve ser girado.


### <a name="qubit--qubit"></a>qubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit ao qual a portão deve ser aplicada.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

Equivalente a:

```qsharp
R(PauliZ, theta, qubit);
```