---
uid: Microsoft.Quantum.Canon.ApplyToPartitionC
title: Operação ApplyToPartitionC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToPartitionC
qsharp.summary: Applies a pair of operations to a given partition of a register into two parts. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 43cf43fa2bf9c00a4096b39555b8f6080dd506d6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850520"
---
# <a name="applytopartitionc-operation"></a>Operação ApplyToPartitionC

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica um par de operações a uma determinada partição de um registro em duas partes.
O modificador `C` indica que a operação é controlável.

```qsharp
operation ApplyToPartitionC (op : ((Qubit[], Qubit[]) => Unit is Ctl), numberOfQubitsToFirstArgument : Int, target : Qubit[]) : Unit is Ctl
```


## <a name="input"></a>Entrada

### <a name="op--qubitqubit--unit--is-ctl"></a>op: ([qubit](xref:microsoft.quantum.lang-ref.qubit)[],[qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é CTL

O par de operações a serem aplicadas à partição especificada.


### <a name="numberofqubitstofirstargument--int"></a>numberOfQubitsToFirstArgument: [int](xref:microsoft.quantum.lang-ref.int)

Número de qubits do destino a ser colocado na primeira parte da partição.
O qubits restante constitui a segunda parte da partição.


### <a name="target--qubit"></a>destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Um registro de qubits que estão sendo particionados e operados pela determinada operação.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ApplyToPartition](xref:Microsoft.Quantum.Canon.ApplyToPartition)