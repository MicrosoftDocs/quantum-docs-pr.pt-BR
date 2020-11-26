---
uid: Microsoft.Quantum.Simulation.AddGeneratorSystems
title: Função AddGeneratorSystems
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: AddGeneratorSystems
qsharp.summary: Adds two `GeneratorSystem`s to create a new `GeneratorSystem`.
ms.openlocfilehash: d6e8f7085cf0558960d055dbeeb08740c3fab049
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229657"
---
# <a name="addgeneratorsystems-function"></a><span data-ttu-id="be200-102">Função AddGeneratorSystems</span><span class="sxs-lookup"><span data-stu-id="be200-102">AddGeneratorSystems function</span></span>

<span data-ttu-id="be200-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="be200-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="be200-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="be200-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="be200-105">Adiciona dois `GeneratorSystem` s para criar um novo `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="be200-105">Adds two `GeneratorSystem`s to create a new `GeneratorSystem`.</span></span>

```qsharp
function AddGeneratorSystems (generatorSystemA : Microsoft.Quantum.Simulation.GeneratorSystem, generatorSystemB : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="be200-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="be200-106">Input</span></span>

### <a name="generatorsystema--generatorsystem"></a><span data-ttu-id="be200-107">generatorSystemA: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="be200-107">generatorSystemA : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="be200-108">O primeiro `GeneratorSystem`.</span><span class="sxs-lookup"><span data-stu-id="be200-108">The first `GeneratorSystem`.</span></span>


### <a name="generatorsystemb--generatorsystem"></a><span data-ttu-id="be200-109">generatorSystemB: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="be200-109">generatorSystemB : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="be200-110">O segundo `GeneratorSystem`.</span><span class="sxs-lookup"><span data-stu-id="be200-110">The second `GeneratorSystem`.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="be200-111">Saída: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="be200-111">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="be200-112">Um que `GeneratorSystem` representa um sistema que é a soma dos sistemas do gerador de entrada.</span><span class="sxs-lookup"><span data-stu-id="be200-112">A `GeneratorSystem` representing a system that is the sum of the input generator systems.</span></span>

## <a name="see-also"></a><span data-ttu-id="be200-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="be200-113">See Also</span></span>

- [<span data-ttu-id="be200-114">Microsoft. Quantum. Simulation. GeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="be200-114">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)