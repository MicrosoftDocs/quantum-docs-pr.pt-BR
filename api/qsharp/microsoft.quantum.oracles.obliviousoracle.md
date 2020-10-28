---
uid: Microsoft.Quantum.Oracles.ObliviousOracle
title: Tipo definido pelo usuário ObliviousOracle
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ObliviousOracle
qsharp.summary: >-
  Represents an oracle for oblivious amplitude amplification.

  The inputs to the oracle $O$ are:

  - The ancilla register $a$ that $O$ acts on. - The system register $s$ on which the desired unitary $U$ is applied, post-selected on register $a$ being in state $\ket{t}\_a$.
ms.openlocfilehash: 7c5b35984f3c8828a5ba9bdae8f9effbc1d378f2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693268"
---
# <a name="obliviousoracle-user-defined-type"></a><span data-ttu-id="28bfd-102">Tipo definido pelo usuário ObliviousOracle</span><span class="sxs-lookup"><span data-stu-id="28bfd-102">ObliviousOracle user defined type</span></span>

<span data-ttu-id="28bfd-103">Namespace: [Microsoft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="28bfd-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="28bfd-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="28bfd-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="28bfd-105">Representa um Oracle para amplificação de amplitude de alheios.</span><span class="sxs-lookup"><span data-stu-id="28bfd-105">Represents an oracle for oblivious amplitude amplification.</span></span>

<span data-ttu-id="28bfd-106">As entradas para o Oracle $O $ são:</span><span class="sxs-lookup"><span data-stu-id="28bfd-106">The inputs to the oracle $O$ are:</span></span>

- <span data-ttu-id="28bfd-107">O ancilla registra $a $ que $O $ age.</span><span class="sxs-lookup"><span data-stu-id="28bfd-107">The ancilla register $a$ that $O$ acts on.</span></span>
- <span data-ttu-id="28bfd-108">O sistema registra $s $ em que o unitário desejado $U $ é aplicado, post-Selected no registro $a $ estando no estado $ \ket{t} \_ a $.</span><span class="sxs-lookup"><span data-stu-id="28bfd-108">The system register $s$ on which the desired unitary $U$ is applied, post-selected on register $a$ being in state $\ket{t}\_a$.</span></span>

```qsharp

newtype ObliviousOracle = (((Qubit[], Qubit[]) => Unit is Adj + Ctl));
```



## <a name="remarks"></a><span data-ttu-id="28bfd-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="28bfd-109">Remarks</span></span>

<span data-ttu-id="28bfd-110">Este Oracle definido por $ $ O\ket {s} \_ a\ket {\ psi} \_ s = \lambda\ket{t} \_ U \ket{\psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket{t ^ \perp} \_ a\cdots $ $ age no ancilla State $ \ket{s} a \_ $ para implementar o unitário $U $ em qualquer estado do sistema $ \ket{\psi} s $ \_ com amplitude $ \lambda $ na base sinalizada por $ \ket{t} \_ a $.</span><span class="sxs-lookup"><span data-stu-id="28bfd-110">This oracle defined by $$ O\ket{s}\_a\ket{\psi}\_s= \lambda\ket{t}\_a U \ket{\psi}\_s + \sqrt{1-|\lambda|^2}\ket{t^\perp}\_a\cdots $$ acts on the ancilla state $\ket{s}\_a$ to implement the unitary $U$ on any system state $\ket{\psi}\_s$ with amplitude $\lambda$ in the basis flagged by $\ket{t}\_a$.</span></span>
<span data-ttu-id="28bfd-111">O primeiro parâmetro é o registro qubit de $ \ket{s} \_ a $.</span><span class="sxs-lookup"><span data-stu-id="28bfd-111">The first parameter is the qubit register of $\ket{s}\_a$.</span></span> <span data-ttu-id="28bfd-112">O segundo parâmetro é o registro qubit de $ \ket{\psi} \_ s $.</span><span class="sxs-lookup"><span data-stu-id="28bfd-112">The second parameter is the qubit register of $\ket{\psi}\_s$.</span></span>