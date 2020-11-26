---
uid: Microsoft.Quantum.Preparation.PurifiedMixedStateRequirements
title: Função PurifiedMixedStateRequirements
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PurifiedMixedStateRequirements
qsharp.summary: Returns the total number of qubits that must be allocated in order to apply the operation returned by @"microsoft.quantum.preparation.purifiedmixedstate".
ms.openlocfilehash: 9b8861a4112c4e6c9db994339353c771a3de81a6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229980"
---
# <a name="purifiedmixedstaterequirements-function"></a>Função PurifiedMixedStateRequirements

Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna o número total de qubits que deve ser alocado para aplicar a operação retornada por @"microsoft.quantum.preparation.purifiedmixedstate" .

```qsharp
function PurifiedMixedStateRequirements (targetError : Double, nCoefficients : Int) : Microsoft.Quantum.Preparation.MixedStatePreparationRequirements
```


## <a name="input"></a>Entrada

### <a name="targeterror--double"></a>targetError: [Double](xref:microsoft.quantum.lang-ref.double)

O erro de destino $ \epsilon $.


### <a name="ncoefficients--int"></a>nCoefficients: [int](xref:microsoft.quantum.lang-ref.int)

O número de coeficientes a ser especificado na preparação de um estado misto.



## <a name="output--mixedstatepreparationrequirements"></a>Saída: [MixedStatePreparationRequirements](xref:Microsoft.Quantum.Preparation.MixedStatePreparationRequirements)

Uma descrição de quantas qubits são necessárias no total e para cada um dos registros de índice e lixo usados pela @"microsoft.quantum.preparation.purifiedmixedstate" função.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Preparation. PurifiedMixedState](xref:Microsoft.Quantum.Preparation.PurifiedMixedState)