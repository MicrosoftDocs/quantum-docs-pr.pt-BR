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
# <a name="generatorindex-user-defined-type"></a>Tipo definido pelo usuário GeneratorIndex

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Agrupa [](https://nuget.org/packages/)


Representa um único termo primitivo no conjunto de todos os geradores dinâmicos, por exemplo, operadores Hermitian, para os quais existe um mapa desse gerador para a evolução de tempo por esse gerador, por meio de `EvolutionSet` .

O primeiro elemento (int [], Double []) é o índice de um único termo, por exemplo, a cadeia de caracteres Pauli XXY com o coeficiente 0,5 seria indexada por ([1, 1, 2], [0,5]). Como alternativa, o Hamiltonians parametrizado por uma variável contínua, como X cos φ + Y Sin φ, pode, por exemplo, ser representado por ([], [φ]). O segundo elemento indexa o subsistema no qual o gerador atua.

```qsharp

newtype GeneratorIndex = ((Int[], Double[]), Int[]);
```



## <a name="remarks"></a>Comentários

> [!WARNING]
> A interpretação de um `GeneratorIndex` não é definida, exceto com referência a um conjunto específico de geradores.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Simulation. Evolucionárioset](xref:Microsoft.Quantum.Simulation.EvolutionSet)
- [Microsoft. Quantum. Simulation. PauliEvolutionSet](xref:Microsoft.Quantum.Simulation.PauliEvolutionSet)