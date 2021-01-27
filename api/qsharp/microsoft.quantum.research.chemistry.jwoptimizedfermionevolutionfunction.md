---
uid: Microsoft.Quantum.Research.Chemistry.JWOptimizedFermionEvolutionFunction
title: Função JWOptimizedFermionEvolutionFunction
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: JWOptimizedFermionEvolutionFunction
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the JWOptimized basis.
ms.openlocfilehash: d70bea8fcb5bd82ddad6dcd2b67c3eb178283bb3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857872"
---
# <a name="jwoptimizedfermionevolutionfunction-function"></a><span data-ttu-id="cd1f0-102">Função JWOptimizedFermionEvolutionFunction</span><span class="sxs-lookup"><span data-stu-id="cd1f0-102">JWOptimizedFermionEvolutionFunction function</span></span>

<span data-ttu-id="cd1f0-103">Namespace: [Microsoft. Quantum. Research. química](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="cd1f0-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="cd1f0-104">Pacote: [Microsoft. Quantum. Research. química](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="cd1f0-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="cd1f0-105">Representa um gerador dinâmico como um conjunto de Gates e uma expansão na base JWOptimized.</span><span class="sxs-lookup"><span data-stu-id="cd1f0-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the JWOptimized basis.</span></span>

```qsharp
function JWOptimizedFermionEvolutionFunction (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex, parityQubit : Qubit) : Microsoft.Quantum.Simulation.EvolutionUnitary
```


## <a name="input"></a><span data-ttu-id="cd1f0-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="cd1f0-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="cd1f0-107">generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="cd1f0-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="cd1f0-108">Um índice de gerador a ser representado como uma evolução unitário na base JWOptimized.</span><span class="sxs-lookup"><span data-stu-id="cd1f0-108">A generator index to be represented as unitary evolution in the JWOptimized basis.</span></span>


### <a name="parityqubit--qubit"></a><span data-ttu-id="cd1f0-109">parityQubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="cd1f0-109">parityQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="cd1f0-110">Qubit que determina o sinal de tempo de evolução.</span><span class="sxs-lookup"><span data-stu-id="cd1f0-110">Qubit that determines the sign of time-evolution.</span></span>



## <a name="output--evolutionunitary"></a><span data-ttu-id="cd1f0-111">Saída: [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span><span class="sxs-lookup"><span data-stu-id="cd1f0-111">Output : [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span></span>

<span data-ttu-id="cd1f0-112">Um `EvolutionUnitary` representando a evolução do tempo pelo termo referenciado em ' generatorIndex.</span><span class="sxs-lookup"><span data-stu-id="cd1f0-112">An `EvolutionUnitary` representing time-evolution by the term referenced in \`generatorIndex.</span></span>