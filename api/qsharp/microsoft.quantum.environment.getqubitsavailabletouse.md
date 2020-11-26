---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToUse
title: Operação GetQubitsAvailableToUse
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToUse
qsharp.summary: Returns the number of qubits currently available to use.
ms.openlocfilehash: ce461b03a08b4c83b9de142c957ce5c590fe9659
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201403"
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