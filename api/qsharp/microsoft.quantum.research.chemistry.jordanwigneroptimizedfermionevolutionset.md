---
uid: Microsoft.Quantum.Research.Chemistry.JordanWignerOptimizedFermionEvolutionSet
title: Função JordanWignerOptimizedFermionEvolutionSet
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: JordanWignerOptimizedFermionEvolutionSet
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.
ms.openlocfilehash: d2d916655b7538b39d5739d67dbb3fc9920cf67a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694944"
---
# <a name="jordanwigneroptimizedfermionevolutionset-function"></a><span data-ttu-id="dffc1-102">Função JordanWignerOptimizedFermionEvolutionSet</span><span class="sxs-lookup"><span data-stu-id="dffc1-102">JordanWignerOptimizedFermionEvolutionSet function</span></span>

<span data-ttu-id="dffc1-103">Namespace: [Microsoft. Quantum. Research. química](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="dffc1-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="dffc1-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dffc1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dffc1-105">Representa um gerador dinâmico como um conjunto de Gates e uma expansão na base Pauli.</span><span class="sxs-lookup"><span data-stu-id="dffc1-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.</span></span>

```qsharp
function JordanWignerOptimizedFermionEvolutionSet (parityQubit : Qubit) : Microsoft.Quantum.Simulation.EvolutionSet
```


## <a name="input"></a><span data-ttu-id="dffc1-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="dffc1-106">Input</span></span>

### <a name="parityqubit--qubit"></a><span data-ttu-id="dffc1-107">parityQubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="dffc1-107">parityQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="dffc1-108">Qubit que determina o sinal de tempo de evolução.</span><span class="sxs-lookup"><span data-stu-id="dffc1-108">Qubit that determines the sign of time-evolution.</span></span>



## <a name="output--evolutionset"></a><span data-ttu-id="dffc1-109">Saída: [evolucionárioset](xref:Microsoft.Quantum.Simulation.EvolutionSet)</span><span class="sxs-lookup"><span data-stu-id="dffc1-109">Output : [EvolutionSet](xref:Microsoft.Quantum.Simulation.EvolutionSet)</span></span>

<span data-ttu-id="dffc1-110">Um `EvolutionSet` que mapeia um `GeneratorIndex` para a base JWOptimized para um ' EvolutionUnitary.</span><span class="sxs-lookup"><span data-stu-id="dffc1-110">An `EvolutionSet` that maps a `GeneratorIndex` for the JWOptimized basis to an \`EvolutionUnitary.</span></span>