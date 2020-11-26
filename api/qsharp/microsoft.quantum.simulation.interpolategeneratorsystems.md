---
uid: Microsoft.Quantum.Simulation.InterpolateGeneratorSystems
title: Função InterpolateGeneratorSystems
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: InterpolateGeneratorSystems
qsharp.summary: Returns a `TimeDependentGeneratorSystem` representing the linear interpolation between two `GeneratorSystem`s.
ms.openlocfilehash: ee47637996313fe1b77c76f00b08417dac956247
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230575"
---
# <a name="interpolategeneratorsystems-function"></a><span data-ttu-id="5273a-102">Função InterpolateGeneratorSystems</span><span class="sxs-lookup"><span data-stu-id="5273a-102">InterpolateGeneratorSystems function</span></span>

<span data-ttu-id="5273a-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="5273a-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="5273a-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5273a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5273a-105">Retorna um `TimeDependentGeneratorSystem` representando a interpolação linear entre dois `GeneratorSystem` s.</span><span class="sxs-lookup"><span data-stu-id="5273a-105">Returns a `TimeDependentGeneratorSystem` representing the linear interpolation between two `GeneratorSystem`s.</span></span>

```qsharp
function InterpolateGeneratorSystems (generatorSystemStart : Microsoft.Quantum.Simulation.GeneratorSystem, generatorSystemEnd : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem
```


## <a name="input"></a><span data-ttu-id="5273a-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="5273a-106">Input</span></span>

### <a name="generatorsystemstart--generatorsystem"></a><span data-ttu-id="5273a-107">generatorSystemStart: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="5273a-107">generatorSystemStart : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="5273a-108">O início `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="5273a-108">The start `GeneratorSystem`.</span></span>


### <a name="generatorsystemend--generatorsystem"></a><span data-ttu-id="5273a-109">generatorSystemEnd: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="5273a-109">generatorSystemEnd : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="5273a-110">O final `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="5273a-110">The end `GeneratorSystem`.</span></span>



## <a name="output--timedependentgeneratorsystem"></a><span data-ttu-id="5273a-111">Saída: [TimeDependentGeneratorSystem](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="5273a-111">Output : [TimeDependentGeneratorSystem](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)</span></span>

<span data-ttu-id="5273a-112">Um que `TimeDependentGeneratorSystem` representa um sistema que é a soma dos sistemas do gerador de entrada, com peso $ (1-s) $ on `generatorSystemStart` e Weight $s $ on `generatorSystemEnd` .</span><span class="sxs-lookup"><span data-stu-id="5273a-112">A `TimeDependentGeneratorSystem` representing a system that is the sum of the input generator systems, with weight $(1-s)$ on `generatorSystemStart` and weight $s$ on `generatorSystemEnd`.</span></span>

## <a name="see-also"></a><span data-ttu-id="5273a-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="5273a-113">See Also</span></span>

- [<span data-ttu-id="5273a-114">Microsoft. Quantum. Simulation. GeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="5273a-114">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)
- [<span data-ttu-id="5273a-115">Microsoft. Quantum. Simulation. TimeDependentGeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="5273a-115">Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)