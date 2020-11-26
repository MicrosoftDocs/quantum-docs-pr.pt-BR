---
uid: Microsoft.Quantum.Oracles.StateOracle
title: Tipo definido pelo usuário StateOracle
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: StateOracle
qsharp.summary: >-
  Represents an oracle for state preparation.

  The inputs to the oracle $O$ are:

  - An integer indexing the flag qubit $f$. - The system register $s$ that will store the desired quantum state $\ket{\psi}\_s$.
ms.openlocfilehash: 6b2cf09c23942a586414daccb99cbb27b5026b9d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226597"
---
# <a name="stateoracle-user-defined-type"></a><span data-ttu-id="606e6-102">Tipo definido pelo usuário StateOracle</span><span class="sxs-lookup"><span data-stu-id="606e6-102">StateOracle user defined type</span></span>

<span data-ttu-id="606e6-103">Namespace: [Microsoft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="606e6-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="606e6-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="606e6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="606e6-105">Representa um Oracle para preparação de estado.</span><span class="sxs-lookup"><span data-stu-id="606e6-105">Represents an oracle for state preparation.</span></span>

<span data-ttu-id="606e6-106">As entradas para o Oracle $O $ são:</span><span class="sxs-lookup"><span data-stu-id="606e6-106">The inputs to the oracle $O$ are:</span></span>

- <span data-ttu-id="606e6-107">Um inteiro que indexa o sinalizador qubit $f $.</span><span class="sxs-lookup"><span data-stu-id="606e6-107">An integer indexing the flag qubit $f$.</span></span>
- <span data-ttu-id="606e6-108">O registro do sistema $s $, que armazenará o estado de Quantum desejado $ \ket{\psi} \_ s $.</span><span class="sxs-lookup"><span data-stu-id="606e6-108">The system register $s$ that will store the desired quantum state $\ket{\psi}\_s$.</span></span>

```qsharp

newtype StateOracle = (((Int, Qubit[]) => Unit is Adj + Ctl));
```



## <a name="remarks"></a><span data-ttu-id="606e6-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="606e6-109">Remarks</span></span>

<span data-ttu-id="606e6-110">Este Oracle definido por $ $ O\ket {0} \_ {f} \ket {0} \_ s = \lambda\ket {1} \_ f\ket {\ psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket {0} \_ f\cdots, $ $ age no estado de base computacional $ \ket {0} \_ {f} \ket {0} \_ s $ para criar o estado de destino $ \ket{\psi} \_ s $ com amplitude $ \lambda $ na base sinalizada por $ \ket {1} \_ f $.</span><span class="sxs-lookup"><span data-stu-id="606e6-110">This oracle defined by $$ O\ket{0}\_{f}\ket{0}\_s= \lambda\ket{1}\_f\ket{\psi}\_s + \sqrt{1-|\lambda|^2}\ket{0}\_f\cdots, $$ acts on the on computational basis state $\ket{0}\_{f}\ket{0}\_s$ to create the target state $\ket{\psi}\_s$ with amplitude $\lambda$ in the basis flagged by $\ket{1}\_f$.</span></span>
<span data-ttu-id="606e6-111">O primeiro parâmetro é um índice para o registro qubit de $ \ket {0} \_ f $.</span><span class="sxs-lookup"><span data-stu-id="606e6-111">The first parameter is an index to the qubit register of $\ket{0}\_f$.</span></span> <span data-ttu-id="606e6-112">O segundo parâmetro abrange ambos os registros.</span><span class="sxs-lookup"><span data-stu-id="606e6-112">The second parameter encompassed both registers.</span></span>