---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToUse
title: Operação GetQubitsAvailableToUse
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToUse
qsharp.summary: Returns the number of qubits currently available to use.
ms.openlocfilehash: 2ed8c3789331a15b351769be960d06f6364d8047
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98827794"
---
# <a name="getqubitsavailabletouse-operation"></a>Operação GetQubitsAvailableToUse

Namespace: [Microsoft. Quantum. Environment](xref:Microsoft.Quantum.Environment)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Retorna o número de qubits disponíveis no momento para uso.

```qsharp
operation GetQubitsAvailableToUse () : Int
```


## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)

O número de qubits que podem ser alocados em uma `using` instrução.
Se o computador de destino que está sendo usado não fornecer essas informações, `-1` será retornado.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Environment. GetQubitsAvailableToBorrow](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow)