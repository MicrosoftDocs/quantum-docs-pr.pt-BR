---
uid: Microsoft.Quantum.Simulation.GeneratorIndex
title: Tipo definido pelo usuário GeneratorIndex
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GeneratorIndex
qsharp.summary: >-
  Represents a single primitive term in the set of all dynamical generators, e.g. Hermitian operators, for which there exists a map from that generator to time-evolution by that generator, through `EvolutionSet`.

  The first element (Int[], Double[]) is indexes that single term -- For instance, the Pauli string XXY with coefficient 0.5 would be indexed by ([1,1,2], [0.5]). Alternatively, Hamiltonians parameterized by a continuous variable, such as X cos φ + Y sin φ, might for instance be represented by ([], [φ]). The second element indexes the subsystem on which the generator acts on.
ms.openlocfilehash: 762dac81ea0963443f0338cea1b879856c84b0ff
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858375"
---
# <a name="generatorindex-user-defined-type"></a><span data-ttu-id="cf5f5-102">Tipo definido pelo usuário GeneratorIndex</span><span class="sxs-lookup"><span data-stu-id="cf5f5-102">GeneratorIndex user defined type</span></span>

<span data-ttu-id="cf5f5-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="cf5f5-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="cf5f5-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cf5f5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cf5f5-105">Representa um único termo primitivo no conjunto de todos os geradores dinâmicos, por exemplo, operadores Hermitian, para os quais existe um mapa desse gerador para a evolução de tempo por esse gerador, por meio de `EvolutionSet` .</span><span class="sxs-lookup"><span data-stu-id="cf5f5-105">Represents a single primitive term in the set of all dynamical generators, e.g. Hermitian operators, for which there exists a map from that generator to time-evolution by that generator, through `EvolutionSet`.</span></span>

<span data-ttu-id="cf5f5-106">O primeiro elemento (int [], Double []) é o índice de um único termo, por exemplo, a cadeia de caracteres Pauli XXY com o coeficiente 0,5 seria indexada por ([1, 1, 2], [0,5]).</span><span class="sxs-lookup"><span data-stu-id="cf5f5-106">The first element (Int[], Double[]) is indexes that single term -- For instance, the Pauli string XXY with coefficient 0.5 would be indexed by ([1,1,2], [0.5]).</span></span> <span data-ttu-id="cf5f5-107">Como alternativa, o Hamiltonians parametrizado por uma variável contínua, como X cos φ + Y Sin φ, pode, por exemplo, ser representado por ([], [φ]).</span><span class="sxs-lookup"><span data-stu-id="cf5f5-107">Alternatively, Hamiltonians parameterized by a continuous variable, such as X cos φ + Y sin φ, might for instance be represented by ([], [φ]).</span></span> <span data-ttu-id="cf5f5-108">O segundo elemento indexa o subsistema no qual o gerador atua.</span><span class="sxs-lookup"><span data-stu-id="cf5f5-108">The second element indexes the subsystem on which the generator acts on.</span></span>

```qsharp

newtype GeneratorIndex = ((Int[], Double[]), Int[]);
```



## <a name="example"></a><span data-ttu-id="cf5f5-109">Exemplo</span><span class="sxs-lookup"><span data-stu-id="cf5f5-109">Example</span></span>

<span data-ttu-id="cf5f5-110">Usando  <xref:microsoft.quantum.simulation.paulievolutionset> o, o operador $ \pi X_2 X_5 Y_9 $ é representado como:</span><span class="sxs-lookup"><span data-stu-id="cf5f5-110">Using  <xref:microsoft.quantum.simulation.paulievolutionset>, the operator $\pi X_2 X_5 Y_9$ is represented as:</span></span>

```qsharp
let index = GeneratorIndex(([1, 1, 2], [PI()]), [2, 5, 9]);
```

## <a name="remarks"></a><span data-ttu-id="cf5f5-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf5f5-111">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="cf5f5-112">A interpretação de um `GeneratorIndex` não é definida, exceto com referência a um conjunto específico de geradores.</span><span class="sxs-lookup"><span data-stu-id="cf5f5-112">The interpretation of an `GeneratorIndex` is not defined except with reference to a particular set of generators.</span></span>

## <a name="see-also"></a><span data-ttu-id="cf5f5-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="cf5f5-113">See Also</span></span>

- [<span data-ttu-id="cf5f5-114">Microsoft. Quantum. Simulation. Evolucionárioset</span><span class="sxs-lookup"><span data-stu-id="cf5f5-114">Microsoft.Quantum.Simulation.EvolutionSet</span></span>](xref:Microsoft.Quantum.Simulation.EvolutionSet)
- [<span data-ttu-id="cf5f5-115">Microsoft. Quantum. Simulation. PauliEvolutionSet</span><span class="sxs-lookup"><span data-stu-id="cf5f5-115">Microsoft.Quantum.Simulation.PauliEvolutionSet</span></span>](xref:Microsoft.Quantum.Simulation.PauliEvolutionSet)