---
uid: Microsoft.Quantum.Canon.ApplyToEachIndex
title: Operação ApplyToEachIndex
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndex
qsharp.summary: Applies a single-qubit operation to each indexed element in a register.
ms.openlocfilehash: 746bc19f7a137ef476a25abdabc4737ed6727ff2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217604"
---
# <a name="applytoeachindex-operation"></a>Operação ApplyToEachIndex

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma operação single-qubit para cada elemento indexado em um registro.

```qsharp
operation ApplyToEachIndex<'T> (singleElementOperation : ((Int, 'T) => Unit), register : 'T[]) : Unit
```


## <a name="input"></a>Entrada

### <a name="singleelementoperation--intt--unit"></a>singleElementOperation: ([int](xref:microsoft.quantum.lang-ref.int), t) = [unidade](xref:microsoft.quantum.lang-ref.unit) de> 

Operação a ser aplicada a cada qubit.


### <a name="register--t"></a>registrar: t []

Matriz de qubits na qual aplicar a operação especificada.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O destino no qual cada uma das operações atua.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ApplyToEach](xref:Microsoft.Quantum.Canon.ApplyToEach)
- [Microsoft. Quantum. Canon. ApplyToEachIndexA](xref:Microsoft.Quantum.Canon.ApplyToEachIndexA)
- [Microsoft. Quantum. Canon. ApplyToEachIndexC](xref:Microsoft.Quantum.Canon.ApplyToEachIndexC)
- [Microsoft. Quantum. Canon. ApplyToEachIndexCA](xref:Microsoft.Quantum.Canon.ApplyToEachIndexCA)