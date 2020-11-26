---
uid: Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsC
title: Operação ApplyToFirstTwoQubitsC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstTwoQubitsC
qsharp.summary: Applies an operation to the first two qubits in the register. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 6b6ee5f05ace92c15ce2038e2fedbaa2fee3dcc9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217349"
---
# <a name="applytofirsttwoqubitsc-operation"></a>Operação ApplyToFirstTwoQubitsC

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma operação às duas primeiras qubits no registro.
O modificador `C` indica que a operação é controlável.

```qsharp
operation ApplyToFirstTwoQubitsC (op : ((Qubit, Qubit) => Unit is Ctl), register : Qubit[]) : Unit is Ctl
```


## <a name="input"></a>Entrada

### <a name="op--qubitqubit--unit--is-ctl"></a>op: ([qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é CTL

Uma operação a ser aplicada às duas primeiras qubits


### <a name="register--qubit"></a>registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Matriz qubit para as duas primeiras qubits das quais a operação é aplicada.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

Isso é equivalente a:

```qsharp
op(register[0], register[1]);
```

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ApplyToFirstTwoQubits](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubits)