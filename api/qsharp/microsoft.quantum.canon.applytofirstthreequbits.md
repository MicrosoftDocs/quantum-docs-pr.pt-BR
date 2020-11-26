---
uid: Microsoft.Quantum.Canon.ApplyToFirstThreeQubits
title: Operação ApplyToFirstThreeQubits
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstThreeQubits
qsharp.summary: Applies an operation to the first three qubits in the register.
ms.openlocfilehash: 5572bd2a096a4f9bdb1153ae80950ae854965b82
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217450"
---
# <a name="applytofirstthreequbits-operation"></a>Operação ApplyToFirstThreeQubits

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma operação às três primeiras qubits no registro.

```qsharp
operation ApplyToFirstThreeQubits (op : ((Qubit, Qubit, Qubit) => Unit), register : Qubit[]) : Unit
```


## <a name="input"></a>Entrada

### <a name="op--qubitqubitqubit--unit"></a>op: ([qubit](xref:microsoft.quantum.lang-ref.qubit),[qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) = [unidade](xref:microsoft.quantum.lang-ref.unit) de> 

Uma operação a ser aplicada aos três primeiros qubits


### <a name="register--qubit"></a>registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Matriz qubit para os três primeiros qubits dos quais a operação é aplicada.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

Isso é equivalente a:

```qsharp
op(register[0], register[1], register[2]);
```

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ApplyToFirstThreeQubitsC](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsC)
- [Microsoft. Quantum. Canon. ApplyToFirstThreeQubitsA](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsA)
- [Microsoft. Quantum. Canon. ApplyToFirstThreeQubitsCA](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsCA)