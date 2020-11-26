---
uid: Microsoft.Quantum.Canon.ApplyToEachA
title: Operação ApplyToEachA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachA
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `A` indicates that the single-qubit operation is adjointable.
ms.openlocfilehash: 9819e78760caf6180edc5c2ca5e402060e3029a5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217791"
---
# <a name="applytoeacha-operation"></a>Operação ApplyToEachA

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma operação de qubit único a cada elemento em um registro.
O modificador `A` indica que a operação single-qubit é o adjointable.

```qsharp
operation ApplyToEachA<'T> (singleElementOperation : ('T => Unit is Adj), register : 'T[]) : Unit is Adj
```


## <a name="input"></a>Entrada

### <a name="singleelementoperation--t--unit--is-adj"></a>singleElementOperation: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj

Operação a ser aplicada a cada qubit.


### <a name="register--t"></a>registrar: t []

Matriz de qubits na qual aplicar a operação especificada.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O destino no qual a operação atua.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ApplyToEach](xref:Microsoft.Quantum.Canon.ApplyToEach)