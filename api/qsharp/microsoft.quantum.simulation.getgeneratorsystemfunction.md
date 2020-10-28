---
uid: Microsoft.Quantum.Simulation.GetGeneratorSystemFunction
title: Função GetGeneratorSystemFunction
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GetGeneratorSystemFunction
qsharp.summary: Retrieves the `GeneratorIndex` function in a `GeneratorSystem`.
ms.openlocfilehash: 60ebbdbd1020d41a54426377043fc0c84ceec504
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696959"
---
# <a name="getgeneratorsystemfunction-function"></a><span data-ttu-id="e9689-102">Função GetGeneratorSystemFunction</span><span class="sxs-lookup"><span data-stu-id="e9689-102">GetGeneratorSystemFunction function</span></span>

<span data-ttu-id="e9689-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="e9689-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="e9689-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e9689-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e9689-105">Recupera a `GeneratorIndex` função em um `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="e9689-105">Retrieves the `GeneratorIndex` function in a `GeneratorSystem`.</span></span>

```qsharp
function GetGeneratorSystemFunction (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex)
```


## <a name="input"></a><span data-ttu-id="e9689-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="e9689-106">Input</span></span>

### <a name="generatorsystem--generatorsystem"></a><span data-ttu-id="e9689-107">generatorSystem: [generatorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="e9689-107">generatorSystem : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="e9689-108">O `GeneratorSystem` de interesse.</span><span class="sxs-lookup"><span data-stu-id="e9689-108">The `GeneratorSystem` of interest.</span></span>



## <a name="output--int---generatorindex"></a><span data-ttu-id="e9689-109">Saída: [int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="e9689-109">Output : [Int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="e9689-110">Uma função que indexa cada `GeneratorIndex` termo em um Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="e9689-110">An function that indexes each `GeneratorIndex` term in a Hamiltonian.</span></span>

## <a name="see-also"></a><span data-ttu-id="e9689-111">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e9689-111">See Also</span></span>

- [<span data-ttu-id="e9689-112">Microsoft. Quantum. Simulation. GeneratorIndex</span><span class="sxs-lookup"><span data-stu-id="e9689-112">Microsoft.Quantum.Simulation.GeneratorIndex</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorIndex)
- [<span data-ttu-id="e9689-113">Microsoft. Quantum. Simulation. GeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="e9689-113">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)