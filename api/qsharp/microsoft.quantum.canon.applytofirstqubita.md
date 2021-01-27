---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitA
title: Operação ApplyToFirstQubitA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitA
qsharp.summary: Applies an operation to the first qubit in the register. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 2f96c2a8ed31d295bc127c568e0ca24c267638b5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841443"
---
# <a name="applytofirstqubita-operation"></a>Operação ApplyToFirstQubitA

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma operação ao primeiro qubit no registro.
O modificador `A` indica que a operação é de adjointable.

```qsharp
operation ApplyToFirstQubitA (op : (Qubit => Unit is Adj), register : Qubit[]) : Unit is Adj
```


## <a name="input"></a>Entrada

### <a name="op--qubit--unit--is-adj"></a>op: [](xref:microsoft.quantum.lang-ref.qubit) a => [unidade](xref:microsoft.quantum.lang-ref.unit) qubit é adj

Uma operação a ser aplicada ao primeiro qubit


### <a name="register--qubit"></a>registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Matriz qubit para a primeira qubit da qual a operação é aplicada



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ApplyToFirstQubit](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)