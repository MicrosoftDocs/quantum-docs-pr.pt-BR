---
uid: Microsoft.Quantum.Canon.ApplyToRestC
title: Operação ApplyToRestC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRestC
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: 779c3831b2027a58f97dae9609e96d4d98247da7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208186"
---
# <a name="applytorestc-operation"></a>Operação ApplyToRestC

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma operação a todos, exceto ao primeiro elemento de uma matriz.

```qsharp
operation ApplyToRestC<'T> (op : ('T[] => Unit is Ctl), targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a>Descrição

Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Rest(targets))` .

## <a name="input"></a>Entrada

### <a name="op--t--unit--is-ctl"></a>op: ' t [] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é CTL

Uma operação a ser aplicada.


### <a name="targets--t"></a>destinos: ' t []

Uma matriz de destinos, das quais todos, exceto o primeiro, será aplicado `op` .



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de entrada da operação a ser aplicada.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ApplyToRest](xref:Microsoft.Quantum.Canon.ApplyToRest)
- [Microsoft. Quantum. Canon. ApplyToRestA](xref:Microsoft.Quantum.Canon.ApplyToRestA)
- [Microsoft. Quantum. Canon. ApplyToRestCA](xref:Microsoft.Quantum.Canon.ApplyToRestCA)