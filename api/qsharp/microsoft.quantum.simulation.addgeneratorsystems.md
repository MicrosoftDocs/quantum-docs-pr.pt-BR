---
uid: Microsoft.Quantum.Simulation.AddGeneratorSystems
title: Função AddGeneratorSystems
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: AddGeneratorSystems
qsharp.summary: Adds two `GeneratorSystem`s to create a new `GeneratorSystem`.
ms.openlocfilehash: b23fc89b941a7cdd93ee7938dda50eb14e3ed528
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857931"
---
# <a name="addgeneratorsystems-function"></a><span data-ttu-id="402a8-102">Função AddGeneratorSystems</span><span class="sxs-lookup"><span data-stu-id="402a8-102">AddGeneratorSystems function</span></span>

<span data-ttu-id="402a8-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="402a8-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="402a8-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="402a8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="402a8-105">Adiciona dois `GeneratorSystem` s para criar um novo `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="402a8-105">Adds two `GeneratorSystem`s to create a new `GeneratorSystem`.</span></span>

```qsharp
function AddGeneratorSystems (generatorSystemA : Microsoft.Quantum.Simulation.GeneratorSystem, generatorSystemB : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="402a8-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="402a8-106">Input</span></span>

### <a name="generatorsystema--generatorsystem"></a><span data-ttu-id="402a8-107">generatorSystemA: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="402a8-107">generatorSystemA : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="402a8-108">O primeiro `GeneratorSystem`.</span><span class="sxs-lookup"><span data-stu-id="402a8-108">The first `GeneratorSystem`.</span></span>


### <a name="generatorsystemb--generatorsystem"></a><span data-ttu-id="402a8-109">generatorSystemB: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="402a8-109">generatorSystemB : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="402a8-110">O segundo `GeneratorSystem`.</span><span class="sxs-lookup"><span data-stu-id="402a8-110">The second `GeneratorSystem`.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="402a8-111">Saída: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="402a8-111">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="402a8-112">Um que `GeneratorSystem` representa um sistema que é a soma dos sistemas do gerador de entrada.</span><span class="sxs-lookup"><span data-stu-id="402a8-112">A `GeneratorSystem` representing a system that is the sum of the input generator systems.</span></span>

## <a name="see-also"></a><span data-ttu-id="402a8-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="402a8-113">See Also</span></span>

- [<span data-ttu-id="402a8-114">Microsoft. Quantum. Simulation. GeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="402a8-114">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)