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
# <a name="getgeneratorsystemfunction-function"></a>Função GetGeneratorSystemFunction

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Recupera a `GeneratorIndex` função em um `GeneratorSystem` .

```qsharp
function GetGeneratorSystemFunction (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex)
```


## <a name="input"></a>Entrada

### <a name="generatorsystem--generatorsystem"></a>generatorSystem: [generatorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

O `GeneratorSystem` de interesse.



## <a name="output--int---generatorindex"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

Uma função que indexa cada `GeneratorIndex` termo em um Hamiltonian.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Simulation. GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)
- [Microsoft. Quantum. Simulation. GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)