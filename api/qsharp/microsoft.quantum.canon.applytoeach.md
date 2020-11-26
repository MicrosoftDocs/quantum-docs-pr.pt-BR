---
uid: Microsoft.Quantum.Canon.ApplyToEach
title: Operação ApplyToEach
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEach
qsharp.summary: Applies a single-qubit operation to each element in a register.
ms.openlocfilehash: 11f9363feb38676df3f805496c74036aa96160c1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217859"
---
# <a name="applytoeach-operation"></a>Operação ApplyToEach

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma operação de qubit único a cada elemento em um registro.

```qsharp
operation ApplyToEach<'T> (singleElementOperation : ('T => Unit), register : 'T[]) : Unit
```


## <a name="input"></a>Entrada

### <a name="singleelementoperation--t--unit"></a>singleElementOperation: t = [unidade](xref:microsoft.quantum.lang-ref.unit) de> 

Operação a ser aplicada a cada qubit.


### <a name="register--t"></a>registrar: t []

Matriz de qubits na qual aplicar a operação especificada.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O destino no qual a operação atua.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ApplyToEachC](xref:Microsoft.Quantum.Canon.ApplyToEachC)
- [Microsoft. Quantum. Canon. ApplyToEachA](xref:Microsoft.Quantum.Canon.ApplyToEachA)
- [Microsoft. Quantum. Canon. ApplyToEachCA](xref:Microsoft.Quantum.Canon.ApplyToEachCA)