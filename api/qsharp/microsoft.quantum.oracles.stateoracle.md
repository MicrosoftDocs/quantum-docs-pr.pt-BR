---
uid: Microsoft.Quantum.Oracles.StateOracle
title: Tipo definido pelo usuário StateOracle
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: StateOracle
qsharp.summary: >-
  Represents an oracle for state preparation.

  The inputs to the oracle $O$ are:

  - An integer indexing the flag qubit $f$. - The system register $s$ that will store the desired quantum state $\ket{\psi}\_s$.
ms.openlocfilehash: 65f4edcf2101190da0c6d00eb4dd21881143ceb0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696912"
---
# <a name="stateoracle-user-defined-type"></a>Tipo definido pelo usuário StateOracle

Namespace: [Microsoft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)

Agrupa [](https://nuget.org/packages/)


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