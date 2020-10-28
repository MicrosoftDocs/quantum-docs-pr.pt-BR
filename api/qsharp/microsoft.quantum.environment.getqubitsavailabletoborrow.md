---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow
title: Operação GetQubitsAvailableToBorrow
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToBorrow
qsharp.summary: Returns the number of qubits currently available to borrow. This includes unused qubits; that is, this includes the qubits returned by `GetQubitsAvailableToUse`.
ms.openlocfilehash: cb56ce4aefd7a03c0f0827b8d34688ef17988f56
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693496"
---
# <a name="getqubitsavailabletoborrow-operation"></a>Operação GetQubitsAvailableToBorrow

Namespace: [Microsoft. Quantum. Environment](xref:Microsoft.Quantum.Environment)

Agrupa [](https://nuget.org/packages/)


Retorna o número de qubits disponíveis no momento para o empréstimo.
Isso inclui qubits não utilizados; ou seja, isso inclui o qubits retornado por `GetQubitsAvailableToUse` .

```qsharp
operation GetQubitsAvailableToBorrow () : Int
```


## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)

O número de qubits que podem ser alocados em uma `borrowing` instrução.
Se o computador de destino que está sendo usado não fornecer essas informações, `-1` será retornado.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Environment. GetQubitsAvailableToUse](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToUse)