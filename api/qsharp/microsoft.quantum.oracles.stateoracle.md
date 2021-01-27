---
uid: Microsoft.Quantum.Oracles.StateOracle
title: Tipo definido pelo usuário StateOracle
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: StateOracle
qsharp.summary: >-
  Represents an oracle for state preparation.

  The inputs to the oracle $O$ are:

  - An integer indexing the flag qubit $f$. - The system register $s$ that will store the desired quantum state $\ket{\psi}\_s$.
ms.openlocfilehash: 005d7862214abb3dcb9c0caa006343720d179a52
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854476"
---
# <a name="stateoracle-user-defined-type"></a>Tipo definido pelo usuário StateOracle

Namespace: [Microsoft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Representa um Oracle para preparação de estado.

As entradas para o Oracle $O $ são:

- Um inteiro que indexa o sinalizador qubit $f $.
- O registro do sistema $s $, que armazenará o estado de Quantum desejado $ \ket{\psi} \_ s $.

```qsharp

newtype StateOracle = (((Int, Qubit[]) => Unit is Adj + Ctl));
```



## <a name="remarks"></a>Comentários

Este Oracle definido por $ $ O\ket {0} \_ {f} \ket {0} \_ s = \lambda\ket {1} \_ f\ket {\ psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket {0} \_ f\cdots, $ $ age no estado de base computacional $ \ket {0} \_ {f} \ket {0} \_ s $ para criar o estado de destino $ \ket{\psi} \_ s $ com amplitude $ \lambda $ na base sinalizada por $ \ket {1} \_ f $.
O primeiro parâmetro é um índice para o registro qubit de $ \ket {0} \_ f $. O segundo parâmetro abrange ambos os registros.