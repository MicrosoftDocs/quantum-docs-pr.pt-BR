---
uid: Microsoft.Quantum.Canon.ApplyToEachC
title: Operação ApplyToEachC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachC
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `C` indicates that the single-qubit operation is controllable.
ms.openlocfilehash: 535f815503e20b5cee35f3f273a714203a4baf12
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217774"
---
# <a name="applytoeachc-operation"></a>Operação ApplyToEachC

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma operação de qubit único a cada elemento em um registro.
O modificador `C` indica que a operação de qubit única é controlável.

```qsharp
operation ApplyToEachC<'T> (singleElementOperation : ('T => Unit is Ctl), register : 'T[]) : Unit is Ctl
```


## <a name="input"></a>Entrada

### <a name="singleelementoperation--t--unit--is-ctl"></a>singleElementOperation: T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é CTL

Operação a ser aplicada a cada qubit.


### <a name="register--t"></a>registrar: t []

Matriz de qubits na qual aplicar a operação especificada.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O destino no qual a operação atua.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ApplyToEach](xref:Microsoft.Quantum.Canon.ApplyToEach)