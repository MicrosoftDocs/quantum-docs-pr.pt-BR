---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracle
title: Tipo definido pelo usuário DeterministicStateOracle
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracle
qsharp.summary: >-
  Represents an oracle for deterministic state preparation.

  The input to the oracle $O$ is:

  - The register that will store the desired quantum state $\ket{\psi}\_s$.
ms.openlocfilehash: 6f8f80aacd3386ba61675101acb87e09fff5afff
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193923"
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