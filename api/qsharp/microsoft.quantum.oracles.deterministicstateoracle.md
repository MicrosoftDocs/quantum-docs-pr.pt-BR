---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracle
title: Tipo definido pelo usuário DeterministicStateOracle
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracle
qsharp.summary: >-
  Represents an oracle for deterministic state preparation.

  The input to the oracle $O$ is:

  - The register that will store the desired quantum state $\ket{\psi}\_s$.
ms.openlocfilehash: 10ae9e52f298cdfb92dd6a9e5cf85960bece6800
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842585"
---
# <a name="deterministicstateoracle-user-defined-type"></a>Tipo definido pelo usuário DeterministicStateOracle

Namespace: [Microsoft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Representa um Oracle para preparação de estado determinística.

A entrada para o Oracle $O $ é:

- O registro que armazenará o estado de Quantum desejado $ \ket{\psi} \_ s $.

```qsharp

newtype DeterministicStateOracle = ((Qubit[] => Unit is Adj + Ctl));
```



## <a name="remarks"></a>Comentários

Esse Oracle definido por $O \ket {0} = \ket{\psi} $ age no estado de base computacional $ \ket {0} $ para criar o estado $ \ket{\psi} $.
O primeiro parâmetro é o registro qubit de $ \ket{\psi} $.