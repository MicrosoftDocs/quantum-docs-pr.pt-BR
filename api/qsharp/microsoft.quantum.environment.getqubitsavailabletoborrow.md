---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow
title: Operação GetQubitsAvailableToBorrow
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToBorrow
qsharp.summary: Returns the number of qubits currently available to borrow.
ms.openlocfilehash: f2294fadb9c10d800b7a743fbfe0810f36f18516
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853242"
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