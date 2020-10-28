---
uid: Microsoft.Quantum.Simulation.PauliEvolutionSet
title: Função PauliEvolutionSet
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliEvolutionSet
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.
ms.openlocfilehash: 89c81aca4cfad6087d764ac8f5a0f1426e905e4b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694931"
---
# <a name="paulievolutionset-function"></a>Função PauliEvolutionSet

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Agrupa [](https://nuget.org/packages/)


Representa um gerador dinâmico como um conjunto de Gates e uma expansão na base Pauli.

```qsharp
function PauliEvolutionSet () : Microsoft.Quantum.Simulation.EvolutionSet
```


## <a name="output--evolutionset"></a>Saída: [evolucionárioset](xref:Microsoft.Quantum.Simulation.EvolutionSet)

Um `EvolutionSet` que mapeia um `GeneratorIndex` para a base Pauli para um ' EvolutionUnitary.

## <a name="remarks"></a>Comentários

Isso é obtido pela aplicação parcial do <xref:microsoft.quantum.simulation.paulievolutionfunction> .