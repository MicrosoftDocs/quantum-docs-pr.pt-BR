---
uid: Microsoft.Quantum.Simulation.SumGeneratorSystems
title: Função SumGeneratorSystems
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: SumGeneratorSystems
qsharp.summary: Adds multiple `GeneratorSystem`s to create a new GeneratorSystem.
ms.openlocfilehash: b667a6af313b5bb8950a34a6d0406976bde49311
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694578"
---
# <a name="sumgeneratorsystems-function"></a><span data-ttu-id="778db-102">Função SumGeneratorSystems</span><span class="sxs-lookup"><span data-stu-id="778db-102">SumGeneratorSystems function</span></span>

<span data-ttu-id="778db-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="778db-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="778db-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="778db-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="778db-105">Adiciona vários `GeneratorSystem` s para criar um novo GeneratorSystem.</span><span class="sxs-lookup"><span data-stu-id="778db-105">Adds multiple `GeneratorSystem`s to create a new GeneratorSystem.</span></span>

```qsharp
function SumGeneratorSystems (generatorSystems : Microsoft.Quantum.Simulation.GeneratorSystem[]) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="778db-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="778db-106">Input</span></span>

### <a name="generatorsystems--generatorsystem"></a><span data-ttu-id="778db-107">generatorSystems: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)[]</span><span class="sxs-lookup"><span data-stu-id="778db-107">generatorSystems : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)[]</span></span>

<span data-ttu-id="778db-108">Uma matriz do tipo `GeneratorSystem[]`.</span><span class="sxs-lookup"><span data-stu-id="778db-108">An array of type `GeneratorSystem[]`.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="778db-109">Saída: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="778db-109">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="778db-110">Um que `GeneratorSystem` representa um sistema que é a soma dos sistemas do gerador de entrada.</span><span class="sxs-lookup"><span data-stu-id="778db-110">A `GeneratorSystem` representing a system that is the sum of the input generator systems.</span></span>

## <a name="see-also"></a><span data-ttu-id="778db-111">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="778db-111">See Also</span></span>

- [<span data-ttu-id="778db-112">Microsoft. Quantum. Simulation. GeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="778db-112">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)