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
# <a name="stateoracle-user-defined-type"></a><span data-ttu-id="fd5ce-102">Tipo definido pelo usuário StateOracle</span><span class="sxs-lookup"><span data-stu-id="fd5ce-102">StateOracle user defined type</span></span>

<span data-ttu-id="fd5ce-103">Namespace: [Microsoft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="fd5ce-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="fd5ce-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fd5ce-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fd5ce-105">Representa um Oracle para preparação de estado.</span><span class="sxs-lookup"><span data-stu-id="fd5ce-105">Represents an oracle for state preparation.</span></span>

<span data-ttu-id="fd5ce-106">As entradas para o Oracle $O $ são:</span><span class="sxs-lookup"><span data-stu-id="fd5ce-106">The inputs to the oracle $O$ are:</span></span>

- <span data-ttu-id="fd5ce-107">Um inteiro que indexa o sinalizador qubit $f $.</span><span class="sxs-lookup"><span data-stu-id="fd5ce-107">An integer indexing the flag qubit $f$.</span></span>
- <span data-ttu-id="fd5ce-108">O registro do sistema $s $, que armazenará o estado de Quantum desejado $ \ket{\psi} \_ s $.</span><span class="sxs-lookup"><span data-stu-id="fd5ce-108">The system register $s$ that will store the desired quantum state $\ket{\psi}\_s$.</span></span>

```qsharp

newtype StateOracle = (((Int, Qubit[]) => Unit is Adj + Ctl));
```



## <a name="remarks"></a><span data-ttu-id="fd5ce-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd5ce-109">Remarks</span></span>

<span data-ttu-id="fd5ce-110">Este Oracle definido por $ $ O\ket {0} \_ {f} \ket {0} \_ s = \lambda\ket {1} \_ f\ket {\ psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket {0} \_ f\cdots, $ $ age no estado de base computacional $ \ket {0} \_ {f} \ket {0} \_ s $ para criar o estado de destino $ \ket{\psi} \_ s $ com amplitude $ \lambda $ na base sinalizada por $ \ket {1} \_ f $.</span><span class="sxs-lookup"><span data-stu-id="fd5ce-110">This oracle defined by $$ O\ket{0}\_{f}\ket{0}\_s= \lambda\ket{1}\_f\ket{\psi}\_s + \sqrt{1-|\lambda|^2}\ket{0}\_f\cdots, $$ acts on the on computational basis state $\ket{0}\_{f}\ket{0}\_s$ to create the target state $\ket{\psi}\_s$ with amplitude $\lambda$ in the basis flagged by $\ket{1}\_f$.</span></span>
<span data-ttu-id="fd5ce-111">O primeiro parâmetro é um índice para o registro qubit de $ \ket {0} \_ f $.</span><span class="sxs-lookup"><span data-stu-id="fd5ce-111">The first parameter is an index to the qubit register of $\ket{0}\_f$.</span></span> <span data-ttu-id="fd5ce-112">O segundo parâmetro abrange ambos os registros.</span><span class="sxs-lookup"><span data-stu-id="fd5ce-112">The second parameter encompassed both registers.</span></span>