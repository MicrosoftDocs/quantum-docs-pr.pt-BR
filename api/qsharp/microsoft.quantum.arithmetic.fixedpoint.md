---
uid: Microsoft.Quantum.Arithmetic.FixedPoint
title: Tipo definido pelo usuário FixedPoint
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: FixedPoint
qsharp.summary: Represents a register of qubits encoding a fixed-point number. Consists of an integer that is equal to the number of qubits to the left of the binary point, i.e., qubits of weight greater than or equal to 1, and a quantum register.
ms.openlocfilehash: f1370cd2f8a7d6488ae0f6be841abd95e61f038e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694789"
---
# <a name="fixedpoint-user-defined-type"></a>Tipo definido pelo usuário FixedPoint

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Agrupa [](https://nuget.org/packages/)


Representa um registro da codificação qubits de um número de ponto fixo. Consiste em um inteiro que é igual ao número de qubits à esquerda do ponto binário, ou seja, qubits de peso maior ou igual a 1 e um registro Quantum.

```qsharp

newtype FixedPoint = (Int, Qubit[]);
```

