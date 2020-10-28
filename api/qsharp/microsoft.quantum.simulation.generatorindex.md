---
uid: Microsoft.Quantum.Simulation.GeneratorIndex
title: Tipo definido pelo usuário GeneratorIndex
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GeneratorIndex
qsharp.summary: >-
  Represents a single primitive term in the set of all dynamical generators, e.g. Hermitian operators, for which there exists a map from that generator to time-evolution by that generator, through `EvolutionSet`.

  The first element (Int[], Double[]) is indexes that single term -- For instance, the Pauli string XXY with coefficient 0.5 would be indexed by ([1,1,2], [0.5]). Alternatively, Hamiltonians parameterized by a continuous variable, such as X cos φ + Y sin φ, might for instance be represented by ([], [φ]). The second element indexes the subsystem on which the generator acts on.
ms.openlocfilehash: 8d36f74fbf122469e9e829b950e4ed9a6e3a35a7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696866"
---
# <a name="generatorindex-user-defined-type"></a><span data-ttu-id="a7765-102">Tipo definido pelo usuário GeneratorIndex</span><span class="sxs-lookup"><span data-stu-id="a7765-102">GeneratorIndex user defined type</span></span>

<span data-ttu-id="a7765-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="a7765-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="a7765-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a7765-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a7765-105">Representa um único termo primitivo no conjunto de todos os geradores dinâmicos, por exemplo, operadores Hermitian, para os quais existe um mapa desse gerador para a evolução de tempo por esse gerador, por meio de `EvolutionSet` .</span><span class="sxs-lookup"><span data-stu-id="a7765-105">Represents a single primitive term in the set of all dynamical generators, e.g. Hermitian operators, for which there exists a map from that generator to time-evolution by that generator, through `EvolutionSet`.</span></span>

<span data-ttu-id="a7765-106">O primeiro elemento (int [], Double []) é o índice de um único termo, por exemplo, a cadeia de caracteres Pauli XXY com o coeficiente 0,5 seria indexada por ([1, 1, 2], [0,5]).</span><span class="sxs-lookup"><span data-stu-id="a7765-106">The first element (Int[], Double[]) is indexes that single term -- For instance, the Pauli string XXY with coefficient 0.5 would be indexed by ([1,1,2], [0.5]).</span></span> <span data-ttu-id="a7765-107">Como alternativa, o Hamiltonians parametrizado por uma variável contínua, como X cos φ + Y Sin φ, pode, por exemplo, ser representado por ([], [φ]).</span><span class="sxs-lookup"><span data-stu-id="a7765-107">Alternatively, Hamiltonians parameterized by a continuous variable, such as X cos φ + Y sin φ, might for instance be represented by ([], [φ]).</span></span> <span data-ttu-id="a7765-108">O segundo elemento indexa o subsistema no qual o gerador atua.</span><span class="sxs-lookup"><span data-stu-id="a7765-108">The second element indexes the subsystem on which the generator acts on.</span></span>

```qsharp

newtype GeneratorIndex = ((Int[], Double[]), Int[]);
```



## <a name="remarks"></a><span data-ttu-id="a7765-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7765-109">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="a7765-110">A interpretação de um `GeneratorIndex` não é definida, exceto com referência a um conjunto específico de geradores.</span><span class="sxs-lookup"><span data-stu-id="a7765-110">The interpretation of an `GeneratorIndex` is not defined except with reference to a particular set of generators.</span></span>

## <a name="see-also"></a><span data-ttu-id="a7765-111">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="a7765-111">See Also</span></span>

- [<span data-ttu-id="a7765-112">Microsoft. Quantum. Simulation. Evolucionárioset</span><span class="sxs-lookup"><span data-stu-id="a7765-112">Microsoft.Quantum.Simulation.EvolutionSet</span></span>](xref:Microsoft.Quantum.Simulation.EvolutionSet)
- [<span data-ttu-id="a7765-113">Microsoft. Quantum. Simulation. PauliEvolutionSet</span><span class="sxs-lookup"><span data-stu-id="a7765-113">Microsoft.Quantum.Simulation.PauliEvolutionSet</span></span>](xref:Microsoft.Quantum.Simulation.PauliEvolutionSet)