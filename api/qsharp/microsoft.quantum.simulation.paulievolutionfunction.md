---
uid: Microsoft.Quantum.Simulation.PauliEvolutionFunction
title: Função PauliEvolutionFunction
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliEvolutionFunction
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.
ms.openlocfilehash: 060f4e4f23bb8b47518a3a22bbca8ab0be6e13b7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694631"
---
# <a name="paulievolutionfunction-function"></a>Função PauliEvolutionFunction

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Agrupa [](https://nuget.org/packages/)


Representa um gerador dinâmico como um conjunto de Gates e uma expansão na base Pauli.

```qsharp
function PauliEvolutionFunction (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.EvolutionUnitary
```


## <a name="input"></a>Entrada

### <a name="generatorindex--generatorindex"></a>generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

Um índice de gerador a ser representado como uma evolução unitário na base Pauli.



## <a name="output--evolutionunitary"></a>Saída: [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)

Um `EvolutionUnitary` representando a evolução do tempo pelo termo referenciado em ' generatorIndex.