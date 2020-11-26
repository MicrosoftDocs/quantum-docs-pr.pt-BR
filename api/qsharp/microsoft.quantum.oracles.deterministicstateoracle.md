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
# <a name="deterministicstateoracle-user-defined-type"></a><span data-ttu-id="8894b-102">Tipo definido pelo usuário DeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="8894b-102">DeterministicStateOracle user defined type</span></span>

<span data-ttu-id="8894b-103">Namespace: [Microsoft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="8894b-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="8894b-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8894b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8894b-105">Representa um Oracle para preparação de estado determinística.</span><span class="sxs-lookup"><span data-stu-id="8894b-105">Represents an oracle for deterministic state preparation.</span></span>

<span data-ttu-id="8894b-106">A entrada para o Oracle $O $ é:</span><span class="sxs-lookup"><span data-stu-id="8894b-106">The input to the oracle $O$ is:</span></span>

- <span data-ttu-id="8894b-107">O registro que armazenará o estado de Quantum desejado $ \ket{\psi} \_ s $.</span><span class="sxs-lookup"><span data-stu-id="8894b-107">The register that will store the desired quantum state $\ket{\psi}\_s$.</span></span>

```qsharp

newtype DeterministicStateOracle = ((Qubit[] => Unit is Adj + Ctl));
```



## <a name="remarks"></a><span data-ttu-id="8894b-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="8894b-108">Remarks</span></span>

<span data-ttu-id="8894b-109">Esse Oracle definido por $O \ket {0} = \ket{\psi} $ age no estado de base computacional $ \ket {0} $ para criar o estado $ \ket{\psi} $.</span><span class="sxs-lookup"><span data-stu-id="8894b-109">This oracle defined by $O\ket{0}=\ket{\psi}$ acts on the on computational basis state $\ket{0}$ to create the state $\ket{\psi}$.</span></span>
<span data-ttu-id="8894b-110">O primeiro parâmetro é o registro qubit de $ \ket{\psi} $.</span><span class="sxs-lookup"><span data-stu-id="8894b-110">The first parameter is the qubit register of $\ket{\psi}$.</span></span>