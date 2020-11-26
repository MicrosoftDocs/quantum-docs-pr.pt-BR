---
uid: Microsoft.Quantum.Oracles.ObliviousOracle
title: Tipo definido pelo usuário ObliviousOracle
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ObliviousOracle
qsharp.summary: >-
  Represents an oracle for oblivious amplitude amplification.

  The inputs to the oracle $O$ are:

  - The ancilla register $a$ that $O$ acts on. - The system register $s$ on which the desired unitary $U$ is applied, post-selected on register $a$ being in state $\ket{t}\_a$.
ms.openlocfilehash: 2f92dcb28ec669229dfaf9bcb23eef9234552b8a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193872"
---
# <a name="obliviousoracle-user-defined-type"></a>Tipo definido pelo usuário ObliviousOracle

Namespace: [Microsoft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Representa um Oracle para amplificação de amplitude de alheios.

As entradas para o Oracle $O $ são:

- O ancilla registra $a $ que $O $ age.
- O sistema registra $s $ em que o unitário desejado $U $ é aplicado, post-Selected no registro $a $ estando no estado $ \ket{t} \_ a $.

```qsharp

newtype ObliviousOracle = (((Qubit[], Qubit[]) => Unit is Adj + Ctl));
```



## <a name="remarks"></a>Comentários

Este Oracle definido por $ $ O\ket {s} \_ a\ket {\ psi} \_ s = \lambda\ket{t} \_ U \ket{\psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket{t ^ \perp} \_ a\cdots $ $ age no ancilla State $ \ket{s} a \_ $ para implementar o unitário $U $ em qualquer estado do sistema $ \ket{\psi} s $ \_ com amplitude $ \lambda $ na base sinalizada por $ \ket{t} \_ a $.
O primeiro parâmetro é o registro qubit de $ \ket{s} \_ a $. O segundo parâmetro é o registro qubit de $ \ket{\psi} \_ s $.