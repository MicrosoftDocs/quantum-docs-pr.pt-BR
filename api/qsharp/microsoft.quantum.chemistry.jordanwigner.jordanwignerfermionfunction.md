---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerFermionFunction
title: Função JordanWignerFermionFunction
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JordanWignerFermionFunction
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.
ms.openlocfilehash: 7d29393293acfc1748a1805f339951b1ff0f9b10
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693702"
---
# <a name="jordanwignerfermionfunction-function"></a><span data-ttu-id="222c7-102">Função JordanWignerFermionFunction</span><span class="sxs-lookup"><span data-stu-id="222c7-102">JordanWignerFermionFunction function</span></span>

<span data-ttu-id="222c7-103">Namespace: [Microsoft. Quantum. química. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="222c7-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="222c7-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="222c7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="222c7-105">Representa um gerador dinâmico como um conjunto de Gates e uma expansão na base JordanWigner.</span><span class="sxs-lookup"><span data-stu-id="222c7-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.</span></span>

```qsharp
function JordanWignerFermionFunction (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.EvolutionUnitary
```


## <a name="input"></a><span data-ttu-id="222c7-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="222c7-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="222c7-107">generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="222c7-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="222c7-108">Um índice do gerador a ser representado como uma evolução unitário no JordanWigner.</span><span class="sxs-lookup"><span data-stu-id="222c7-108">A generator index to be represented as unitary evolution in the JordanWigner.</span></span>



## <a name="output--evolutionunitary"></a><span data-ttu-id="222c7-109">Saída: [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span><span class="sxs-lookup"><span data-stu-id="222c7-109">Output : [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span></span>

<span data-ttu-id="222c7-110">Um `EvolutionUnitary` representando a evolução do tempo pelo termo referenciado em ' generatorIndex.</span><span class="sxs-lookup"><span data-stu-id="222c7-110">An `EvolutionUnitary` representing time-evolution by the term referenced in \`generatorIndex.</span></span>