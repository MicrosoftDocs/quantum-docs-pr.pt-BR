---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracle
title: Tipo definido pelo usuário DeterministicStateOracle
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracle
qsharp.summary: >-
  Represents an oracle for deterministic state preparation.

  The input to the oracle $O$ is:

  - The register that will store the desired quantum state $\ket{\psi}\_s$.
ms.openlocfilehash: f02267d48cf42fb5b02782dc6b667ac7b60a05dc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696922"
---
# <a name="deterministicstateoracle-user-defined-type"></a>Tipo definido pelo usuário DeterministicStateOracle

Namespace: [Microsoft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)

Agrupa [](https://nuget.org/packages/)


Representa um Oracle para preparação de estado determinística.

A entrada para o Oracle $O $ é:

- O registro que armazenará o estado de Quantum desejado $ \ket{\psi} \_ s $.

```qsharp

newtype DeterministicStateOracle = ((Qubit[] => Unit is Adj + Ctl));
```



## <a name="remarks"></a>Comentários

Esse Oracle definido por $O \ket {0} = \ket{\psi} $ age no estado de base computacional $ \ket {0} $ para criar o estado $ \ket{\psi} $.
O primeiro parâmetro é o registro qubit de $ \ket{\psi} $.