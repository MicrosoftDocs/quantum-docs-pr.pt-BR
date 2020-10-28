---
uid: Microsoft.Quantum.Research.Chemistry.JordanWignerOptimizedFermionEvolutionSet
title: Função JordanWignerOptimizedFermionEvolutionSet
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: JordanWignerOptimizedFermionEvolutionSet
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.
ms.openlocfilehash: d2d916655b7538b39d5739d67dbb3fc9920cf67a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694944"
---
# <a name="jordanwigneroptimizedfermionevolutionset-function"></a>Função JordanWignerOptimizedFermionEvolutionSet

Namespace: [Microsoft. Quantum. Research. química](xref:Microsoft.Quantum.Research.Chemistry)

Agrupa [](https://nuget.org/packages/)


Representa um gerador dinâmico como um conjunto de Gates e uma expansão na base Pauli.

```qsharp
function JordanWignerOptimizedFermionEvolutionSet (parityQubit : Qubit) : Microsoft.Quantum.Simulation.EvolutionSet
```


## <a name="input"></a>Entrada

### <a name="parityqubit--qubit"></a>parityQubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit que determina o sinal de tempo de evolução.



## <a name="output--evolutionset"></a>Saída: [evolucionárioset](xref:Microsoft.Quantum.Simulation.EvolutionSet)

Um `EvolutionSet` que mapeia um `GeneratorIndex` para a base JWOptimized para um ' EvolutionUnitary.