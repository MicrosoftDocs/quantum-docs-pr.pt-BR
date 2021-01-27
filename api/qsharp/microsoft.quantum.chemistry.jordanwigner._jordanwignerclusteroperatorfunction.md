---
uid: Microsoft.Quantum.Chemistry.JordanWigner._JordanWignerClusterOperatorFunction
title: Função _JordanWignerClusterOperatorFunction
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _JordanWignerClusterOperatorFunction
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.
ms.openlocfilehash: 71aa0256b4d2911fe9d8e3ca091735d6375ed23e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839503"
---
# <a name="_jordanwignerclusteroperatorfunction-function"></a><span data-ttu-id="90254-102">Função _JordanWignerClusterOperatorFunction</span><span class="sxs-lookup"><span data-stu-id="90254-102">_JordanWignerClusterOperatorFunction function</span></span>

<span data-ttu-id="90254-103">Namespace: [Microsoft. Quantum. química. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="90254-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="90254-104">Pacote: [Microsoft. Quantum. química](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="90254-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="90254-105">Representa um gerador dinâmico como um conjunto de Gates e uma expansão na base JordanWigner.</span><span class="sxs-lookup"><span data-stu-id="90254-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.</span></span>

```qsharp
function _JordanWignerClusterOperatorFunction (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.EvolutionUnitary
```


## <a name="input"></a><span data-ttu-id="90254-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="90254-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="90254-107">generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="90254-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="90254-108">Um índice do gerador a ser representado como uma evolução unitário no JordanWigner.</span><span class="sxs-lookup"><span data-stu-id="90254-108">A generator index to be represented as unitary evolution in the JordanWigner.</span></span>



## <a name="output--evolutionunitary"></a><span data-ttu-id="90254-109">Saída: [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span><span class="sxs-lookup"><span data-stu-id="90254-109">Output : [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span></span>

<span data-ttu-id="90254-110">Um `EvolutionUnitary` representando a evolução do tempo pelo termo referenciado em ' generatorIndex.</span><span class="sxs-lookup"><span data-stu-id="90254-110">An `EvolutionUnitary` representing time-evolution by the term referenced in \`generatorIndex.</span></span>