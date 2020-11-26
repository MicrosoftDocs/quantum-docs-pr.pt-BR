---
uid: Microsoft.Quantum.Canon.ApplyToEachIndexA
title: Operação ApplyToEachIndexA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndexA
qsharp.summary: Applies a single-qubit operation to each indexed element in a register. The modifier `A` indicates that the single-qubit operation is adjointable.
ms.openlocfilehash: e3ff812f14181e676fddf436af8a14f9a58271ec
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217587"
---
# <a name="applytoeachindexa-operation"></a>Operação ApplyToEachIndexA

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma operação single-qubit para cada elemento indexado em um registro.
O modificador `A` indica que a operação single-qubit é o adjointable.

```qsharp
operation ApplyToEachIndexA<'T> (singleElementOperation : ((Int, 'T) => Unit is Adj), register : 'T[]) : Unit is Adj
```


## <a name="input"></a>Entrada

### <a name="singleelementoperation--intt--unit--is-adj"></a>singleElementOperation: ([int](xref:microsoft.quantum.lang-ref.int), t) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj

Operação a ser aplicada a cada qubit.


### <a name="register--t"></a>registrar: t []

Matriz de qubits na qual aplicar a operação especificada.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O destino no qual cada uma das operações atua.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ApplyToEachIndex](xref:Microsoft.Quantum.Canon.ApplyToEachIndex)