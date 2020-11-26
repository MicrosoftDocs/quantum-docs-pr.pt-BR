---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow
title: Operação GetQubitsAvailableToBorrow
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToBorrow
qsharp.summary: Returns the number of qubits currently available to borrow.
ms.openlocfilehash: 30b97c2b6e1353f008d085c3bae6160763557c67
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201454"
---
# <a name="getqubitsavailabletoborrow-operation"></a>Operação GetQubitsAvailableToBorrow

Namespace: [Microsoft. Quantum. Environment](xref:Microsoft.Quantum.Environment)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Retorna o número de qubits disponíveis no momento para o empréstimo.

```qsharp
operation GetQubitsAvailableToBorrow () : Int
```


## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)

O número de qubits que podem ser emprestados e não serão alocados como parte de uma `borrowing` instrução.
Se o computador de destino que está sendo usado não fornecer essas informações, `-1` será retornado.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Environment. GetQubitsAvailableToUse](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToUse)