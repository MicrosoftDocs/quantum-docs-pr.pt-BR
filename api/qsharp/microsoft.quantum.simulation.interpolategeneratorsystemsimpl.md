---
uid: Microsoft.Quantum.Simulation.InterpolateGeneratorSystemsImpl
title: Função InterpolateGeneratorSystemsImpl
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: InterpolateGeneratorSystemsImpl
qsharp.summary: Linearly interpolates between two `GeneratorSystems` according to a schedule parameter `s` between 0 and 1 (inclusive).
ms.openlocfilehash: a902a93968d221349f9a6fa977bbc1706971fcfd
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855763"
---
# <a name="interpolategeneratorsystemsimpl-function"></a>Função InterpolateGeneratorSystemsImpl

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Interpola linearmente entre dois `GeneratorSystems` de acordo com um parâmetro de agendamento `s` entre 0 e 1 (inclusivo).

```qsharp
function InterpolateGeneratorSystemsImpl (schedule : Double, generatorSystemStart : Microsoft.Quantum.Simulation.GeneratorSystem, generatorSystemEnd : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a>Entrada

### <a name="schedule--double"></a>agendamento: [duplo](xref:microsoft.quantum.lang-ref.double)

Um parâmetro de agendamento $s na [0, 1] $.


### <a name="generatorsystemstart--generatorsystem"></a>generatorSystemStart: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

O início `GeneratorSystem` .


### <a name="generatorsystemend--generatorsystem"></a>generatorSystemEnd: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

O final `GeneratorSystem` .



## <a name="output--generatorsystem"></a>Saída: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Um que `GeneratorSystem` representa um sistema que é a soma dos sistemas do gerador de entrada, com peso $ (1-s) $ on `generatorSystemStart` e Weight $s $ on `generatorSystemEnd` .

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Simulation. GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)