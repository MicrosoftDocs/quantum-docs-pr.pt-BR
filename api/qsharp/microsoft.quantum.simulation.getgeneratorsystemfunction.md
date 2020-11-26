---
uid: Microsoft.Quantum.Simulation.GetGeneratorSystemFunction
title: Função GetGeneratorSystemFunction
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GetGeneratorSystemFunction
qsharp.summary: Retrieves the `GeneratorIndex` function in a `GeneratorSystem`.
ms.openlocfilehash: 28e3c12d0ae0b08fc368c25eeb6f38d2834ca912
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229300"
---
# <a name="getgeneratorsystemfunction-function"></a><span data-ttu-id="afc22-102">Função GetGeneratorSystemFunction</span><span class="sxs-lookup"><span data-stu-id="afc22-102">GetGeneratorSystemFunction function</span></span>

<span data-ttu-id="afc22-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="afc22-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="afc22-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="afc22-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="afc22-105">Recupera a `GeneratorIndex` função em um `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="afc22-105">Retrieves the `GeneratorIndex` function in a `GeneratorSystem`.</span></span>

```qsharp
function GetGeneratorSystemFunction (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex)
```


## <a name="input"></a><span data-ttu-id="afc22-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="afc22-106">Input</span></span>

### <a name="generatorsystem--generatorsystem"></a><span data-ttu-id="afc22-107">generatorSystem: [generatorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="afc22-107">generatorSystem : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="afc22-108">O `GeneratorSystem` de interesse.</span><span class="sxs-lookup"><span data-stu-id="afc22-108">The `GeneratorSystem` of interest.</span></span>



## <a name="output--int---generatorindex"></a><span data-ttu-id="afc22-109">Saída: [int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="afc22-109">Output : [Int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="afc22-110">Uma função que indexa cada `GeneratorIndex` termo em um Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="afc22-110">An function that indexes each `GeneratorIndex` term in a Hamiltonian.</span></span>

## <a name="see-also"></a><span data-ttu-id="afc22-111">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="afc22-111">See Also</span></span>

- [<span data-ttu-id="afc22-112">Microsoft. Quantum. Simulation. GeneratorIndex</span><span class="sxs-lookup"><span data-stu-id="afc22-112">Microsoft.Quantum.Simulation.GeneratorIndex</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorIndex)
- [<span data-ttu-id="afc22-113">Microsoft. Quantum. Simulation. GeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="afc22-113">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)