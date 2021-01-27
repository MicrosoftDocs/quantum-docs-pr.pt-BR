---
uid: Microsoft.Quantum.Research.Chemistry.JordanWignerOptimizedFermionEvolutionSet
title: Função JordanWignerOptimizedFermionEvolutionSet
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: JordanWignerOptimizedFermionEvolutionSet
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.
ms.openlocfilehash: 941d66a936ef1a2ac76230d14ca8437ac2a4a049
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857895"
---
# <a name="jordanwigneroptimizedfermionevolutionset-function"></a><span data-ttu-id="f7e45-102">Função JordanWignerOptimizedFermionEvolutionSet</span><span class="sxs-lookup"><span data-stu-id="f7e45-102">JordanWignerOptimizedFermionEvolutionSet function</span></span>

<span data-ttu-id="f7e45-103">Namespace: [Microsoft. Quantum. Research. química](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="f7e45-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="f7e45-104">Pacote: [Microsoft. Quantum. Research. química](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="f7e45-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="f7e45-105">Representa um gerador dinâmico como um conjunto de Gates e uma expansão na base Pauli.</span><span class="sxs-lookup"><span data-stu-id="f7e45-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.</span></span>

```qsharp
function JordanWignerOptimizedFermionEvolutionSet (parityQubit : Qubit) : Microsoft.Quantum.Simulation.EvolutionSet
```


## <a name="input"></a><span data-ttu-id="f7e45-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7e45-106">Input</span></span>

### <a name="parityqubit--qubit"></a><span data-ttu-id="f7e45-107">parityQubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f7e45-107">parityQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="f7e45-108">Qubit que determina o sinal de tempo de evolução.</span><span class="sxs-lookup"><span data-stu-id="f7e45-108">Qubit that determines the sign of time-evolution.</span></span>



## <a name="output--evolutionset"></a><span data-ttu-id="f7e45-109">Saída: [evolucionárioset](xref:Microsoft.Quantum.Simulation.EvolutionSet)</span><span class="sxs-lookup"><span data-stu-id="f7e45-109">Output : [EvolutionSet](xref:Microsoft.Quantum.Simulation.EvolutionSet)</span></span>

<span data-ttu-id="f7e45-110">Um `EvolutionSet` que mapeia um `GeneratorIndex` para a base JWOptimized para um ' EvolutionUnitary.</span><span class="sxs-lookup"><span data-stu-id="f7e45-110">An `EvolutionSet` that maps a `GeneratorIndex` for the JWOptimized basis to an \`EvolutionUnitary.</span></span>