---
uid: Microsoft.Quantum.Simulation.EvolutionUnitary
title: Tipo definido pelo usuário EvolutionUnitary
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EvolutionUnitary
qsharp.summary: >-
  Represents a unitary time-evolution operator.

  The first parameter is is duration of time-evolution, and the second parameter is the qubit register acted upon by the unitary.
ms.openlocfilehash: ea160bb9a0a8bb5106c3e37a6a16155bad71dd25
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856053"
---
# <a name="evolutionunitary-user-defined-type"></a><span data-ttu-id="49b62-102">Tipo definido pelo usuário EvolutionUnitary</span><span class="sxs-lookup"><span data-stu-id="49b62-102">EvolutionUnitary user defined type</span></span>

<span data-ttu-id="49b62-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="49b62-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="49b62-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="49b62-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="49b62-105">Representa um operador de evolução de tempo unitário.</span><span class="sxs-lookup"><span data-stu-id="49b62-105">Represents a unitary time-evolution operator.</span></span>

<span data-ttu-id="49b62-106">O primeiro parâmetro é a duração da evolução do tempo e o segundo parâmetro é o registro de qubit acionado pelo unitário.</span><span class="sxs-lookup"><span data-stu-id="49b62-106">The first parameter is is duration of time-evolution, and the second parameter is the qubit register acted upon by the unitary.</span></span>

```qsharp

newtype EvolutionUnitary = (((Double, Qubit[]) => Unit is Adj + Ctl));
```

