---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitC
title: Operação ApplyToFirstQubitC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitC
qsharp.summary: Applies operation op to the first qubit in the register. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 2659c3a97baa68cb4c1d7781381f89742902594d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217502"
---
# <a name="applytofirstqubitc-operation"></a>Operação ApplyToFirstQubitC

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica a operação op para o primeiro qubit no registro.
O modificador `C` indica que a operação é controlável.

```qsharp
operation ApplyToFirstQubitC (op : (Qubit => Unit is Ctl), register : Qubit[]) : Unit is Ctl
```


## <a name="input"></a>Entrada

### <a name="op--qubit--unit--is-ctl"></a>op: [Qubit](xref:microsoft.quantum.lang-ref.qubit) a => [unidade](xref:microsoft.quantum.lang-ref.unit) qubit é CTL

Uma operação a ser aplicada ao primeiro qubit


### <a name="register--qubit"></a>registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Matriz qubit para a primeira qubit da qual a operação é aplicada



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ApplyToFirstQubit](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)