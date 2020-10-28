---
uid: Microsoft.Quantum.Simulation.MultiplyGeneratorIndex
title: Função MultiplyGeneratorIndex
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: MultiplyGeneratorIndex
qsharp.summary: Multiplies the coefficient in a `GeneratorIndex`.
ms.openlocfilehash: 9ee0568073b65b027cc98eb56934e9286b59c27f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696950"
---
# <a name="multiplygeneratorindex-function"></a>Função MultiplyGeneratorIndex

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Agrupa [](https://nuget.org/packages/)


Multiplica o coeficiente em um `GeneratorIndex` .

```qsharp
function MultiplyGeneratorIndex (multiplier : Double, generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a>Entrada

### <a name="multiplier--double"></a>multiplicador: [duplo](xref:microsoft.quantum.lang-ref.double)

O multiplicador no coeficiente.


### <a name="generatorindex--generatorindex"></a>generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

O `GeneratorIndex` a ser multiplicado.



## <a name="output--generatorindex"></a>Saída: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

Um `GeneratorIndex` que representa um termo com o coeficiente um fator `multiplier` maior.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Simulation. GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)