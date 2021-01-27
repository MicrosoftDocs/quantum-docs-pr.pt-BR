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
# <a name="deterministicstateoracle-user-defined-type"></a><span data-ttu-id="f9a0a-102">Tipo definido pelo usuário DeterministicStateOracle</span><span class="sxs-lookup"><span data-stu-id="f9a0a-102">DeterministicStateOracle user defined type</span></span>

<span data-ttu-id="f9a0a-103">Namespace: [Microsoft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="f9a0a-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="f9a0a-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f9a0a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f9a0a-105">Representa um Oracle para preparação de estado determinística.</span><span class="sxs-lookup"><span data-stu-id="f9a0a-105">Represents an oracle for deterministic state preparation.</span></span>

<span data-ttu-id="f9a0a-106">A entrada para o Oracle $O $ é:</span><span class="sxs-lookup"><span data-stu-id="f9a0a-106">The input to the oracle $O$ is:</span></span>

- <span data-ttu-id="f9a0a-107">O registro que armazenará o estado de Quantum desejado $ \ket{\psi} \_ s $.</span><span class="sxs-lookup"><span data-stu-id="f9a0a-107">The register that will store the desired quantum state $\ket{\psi}\_s$.</span></span>

```qsharp

newtype DeterministicStateOracle = ((Qubit[] => Unit is Adj + Ctl));
```



## <a name="remarks"></a><span data-ttu-id="f9a0a-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9a0a-108">Remarks</span></span>

<span data-ttu-id="f9a0a-109">Esse Oracle definido por $O \ket {0} = \ket{\psi} $ age no estado de base computacional $ \ket {0} $ para criar o estado $ \ket{\psi} $.</span><span class="sxs-lookup"><span data-stu-id="f9a0a-109">This oracle defined by $O\ket{0}=\ket{\psi}$ acts on the on computational basis state $\ket{0}$ to create the state $\ket{\psi}$.</span></span>
<span data-ttu-id="f9a0a-110">O primeiro parâmetro é o registro qubit de $ \ket{\psi} $.</span><span class="sxs-lookup"><span data-stu-id="f9a0a-110">The first parameter is the qubit register of $\ket{\psi}$.</span></span>