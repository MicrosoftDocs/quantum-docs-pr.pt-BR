---
uid: Microsoft.Quantum.Intrinsic.S
title: Operação S
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: S
qsharp.summary: Applies the S gate to a single qubit.
ms.openlocfilehash: c697408c4efe1963787b5aee8f0d3bb6b9e64dd5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198445"
---
# <a name="s-operation"></a>Operação S

Namespace: [Microsoft. Quantum. intrínseco](xref:Microsoft.Quantum.Intrinsic)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Aplica o portão S a um único qubit.

```qsharp
operation S (qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>Descrição

Esta operação pode ser simulada pela matriz unitário \begin{align} S \mathrel{: =} \begin{bmatrix} 1 & 0 \\ \\ 0 & i \end{bmatrix}.
\end{align}

## <a name="input"></a>Entrada

### <a name="qubit--qubit"></a>qubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit ao qual a portão deve ser aplicada.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

