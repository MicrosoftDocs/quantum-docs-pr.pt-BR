---
uid: Microsoft.Quantum.Simulation.BlockEncoding
title: Tipo definido pelo usuário BlockEncoding
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncoding
qsharp.summary: >-
  Represents a unitary where an arbitrary operator of interest is encoded in the top-left block.

  That is, a `BlockEncoding` is a unitary $U$ where an arbitrary operator $H$ of interest that acts on the system register `s` is encoded in the top- left block corresponding to auxiliary state $\ket{0}_a$. That is,

  $$ \begin{align} (\bra{0}_a\otimes I_s)U(\ket{0}_a\otimes I_s) = H \end{align} $$.
ms.openlocfilehash: 75fdbf13cf07d906982d4a611d1d25b3e29db2cd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225424"
---
# <a name="blockencoding-user-defined-type"></a><span data-ttu-id="6d0c3-102">Tipo definido pelo usuário BlockEncoding</span><span class="sxs-lookup"><span data-stu-id="6d0c3-102">BlockEncoding user defined type</span></span>

<span data-ttu-id="6d0c3-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="6d0c3-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="6d0c3-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6d0c3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6d0c3-105">Representa um unitário em que um operador arbitrário de interesse é codificado no bloco superior esquerdo.</span><span class="sxs-lookup"><span data-stu-id="6d0c3-105">Represents a unitary where an arbitrary operator of interest is encoded in the top-left block.</span></span>

<span data-ttu-id="6d0c3-106">Ou seja, um `BlockEncoding` é um unitário $U $, em que um operador arbitrário $H $ de interesse que age no registro do sistema `s` é codificado no bloco superior esquerdo correspondente ao estado auxiliar $ \ket {0} _A $.</span><span class="sxs-lookup"><span data-stu-id="6d0c3-106">That is, a `BlockEncoding` is a unitary $U$ where an arbitrary operator $H$ of interest that acts on the system register `s` is encoded in the top- left block corresponding to auxiliary state $\ket{0}_a$.</span></span> <span data-ttu-id="6d0c3-107">Isto é</span><span class="sxs-lookup"><span data-stu-id="6d0c3-107">That is,</span></span>

<span data-ttu-id="6d0c3-108">$ $ \begin{align} (\bra {0} _A \otimes I_s) U (\ket {0} _a \otimes I_s) = H \end{align} $ $.</span><span class="sxs-lookup"><span data-stu-id="6d0c3-108">$$ \begin{align} (\bra{0}_a\otimes I_s)U(\ket{0}_a\otimes I_s) = H \end{align} $$.</span></span>

```qsharp

newtype BlockEncoding = (((Qubit[], Qubit[]) => Unit is Adj + Ctl));
```

