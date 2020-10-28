---
uid: Microsoft.Quantum.Simulation.GeneratorSystem
title: Tipo definido pelo usuário GeneratorSystem
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GeneratorSystem
qsharp.summary: >-
  Represents a collection of `GeneratorIndex`es.

  We iterate over this collection using a single-index integer, and the size of the collection is assumed to be known.
ms.openlocfilehash: c03caf99b197410c7fa15021c8acaaf55a728781
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696960"
---
# <a name="generatorsystem-user-defined-type"></a>Tipo definido pelo usuário GeneratorSystem

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Agrupa [](https://nuget.org/packages/)


Representa uma coleção de `GeneratorIndex` es.

Iteramos essa coleção usando um inteiro de índice único e o tamanho da coleção é considerado conhecido.

```qsharp

newtype GeneratorSystem = (Int, (Int -> Microsoft.Quantum.Simulation.GeneratorIndex));
```



## <a name="remarks"></a>Comentários

As instâncias do `GeneratorSystem` podem ser definidas facilmente usando a <xref:microsoft.quantum.arrays.lookupfunction> função.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. arrays. LookupFunction](xref:Microsoft.Quantum.Arrays.LookupFunction)