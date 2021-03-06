---
uid: Microsoft.Quantum.Arithmetic.FixedPoint
title: Tipo definido pelo usuário FixedPoint
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: FixedPoint
qsharp.summary: Represents a register of qubits encoding a fixed-point number. Consists of an integer that is equal to the number of qubits to the left of the binary point, i.e., qubits of weight greater than or equal to 1, and a quantum register.
ms.openlocfilehash: 18e85120647c5a1f41ccab5fbfb27ea602a279af
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843196"
---
# <a name="fixedpoint-user-defined-type"></a>Tipo definido pelo usuário FixedPoint

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Representa um registro da codificação qubits de um número de ponto fixo. Consiste em um inteiro que é igual ao número de qubits à esquerda do ponto binário, ou seja, qubits de peso maior ou igual a 1 e um registro Quantum.

```qsharp

newtype FixedPoint = (Int, Qubit[]);
```

