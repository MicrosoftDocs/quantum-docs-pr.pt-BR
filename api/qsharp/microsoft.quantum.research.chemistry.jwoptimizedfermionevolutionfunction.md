---
uid: Microsoft.Quantum.Research.Chemistry.JWOptimizedFermionEvolutionFunction
title: Função JWOptimizedFermionEvolutionFunction
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: JWOptimizedFermionEvolutionFunction
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the JWOptimized basis.
ms.openlocfilehash: 952f3dc4ab0595ace0ee34c040cb21969afa111f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693241"
---
# <a name="jwoptimizedfermionevolutionfunction-function"></a><span data-ttu-id="2625d-102">Função JWOptimizedFermionEvolutionFunction</span><span class="sxs-lookup"><span data-stu-id="2625d-102">JWOptimizedFermionEvolutionFunction function</span></span>

<span data-ttu-id="2625d-103">Namespace: [Microsoft. Quantum. Research. química](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="2625d-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="2625d-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2625d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2625d-105">Representa um gerador dinâmico como um conjunto de Gates e uma expansão na base JWOptimized.</span><span class="sxs-lookup"><span data-stu-id="2625d-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the JWOptimized basis.</span></span>

```qsharp
function JWOptimizedFermionEvolutionFunction (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex, parityQubit : Qubit) : Microsoft.Quantum.Simulation.EvolutionUnitary
```


## <a name="input"></a><span data-ttu-id="2625d-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="2625d-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="2625d-107">generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="2625d-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="2625d-108">Um índice de gerador a ser representado como uma evolução unitário na base JWOptimized.</span><span class="sxs-lookup"><span data-stu-id="2625d-108">A generator index to be represented as unitary evolution in the JWOptimized basis.</span></span>


### <a name="parityqubit--qubit"></a><span data-ttu-id="2625d-109">parityQubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="2625d-109">parityQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="2625d-110">Qubit que determina o sinal de tempo de evolução.</span><span class="sxs-lookup"><span data-stu-id="2625d-110">Qubit that determines the sign of time-evolution.</span></span>



## <a name="output--evolutionunitary"></a><span data-ttu-id="2625d-111">Saída: [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span><span class="sxs-lookup"><span data-stu-id="2625d-111">Output : [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span></span>

<span data-ttu-id="2625d-112">Um `EvolutionUnitary` representando a evolução do tempo pelo termo referenciado em ' generatorIndex.</span><span class="sxs-lookup"><span data-stu-id="2625d-112">An `EvolutionUnitary` representing time-evolution by the term referenced in \`generatorIndex.</span></span>