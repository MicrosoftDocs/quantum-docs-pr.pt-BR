---
uid: Microsoft.Quantum.Simulation.GeneratorIndex
title: Tipo definido pelo usuário GeneratorIndex
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GeneratorIndex
qsharp.summary: >-
  Represents a single primitive term in the set of all dynamical generators, e.g. Hermitian operators, for which there exists a map from that generator to time-evolution by that generator, through `EvolutionSet`.

  The first element (Int[], Double[]) is indexes that single term -- For instance, the Pauli string XXY with coefficient 0.5 would be indexed by ([1,1,2], [0.5]). Alternatively, Hamiltonians parameterized by a continuous variable, such as X cos φ + Y sin φ, might for instance be represented by ([], [φ]). The second element indexes the subsystem on which the generator acts on.
ms.openlocfilehash: dae23db9bee34be4aa99d96799efad64a66d7193
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229317"
---
# <a name="generatorindex-user-defined-type"></a>Tipo definido pelo usuário GeneratorIndex

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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