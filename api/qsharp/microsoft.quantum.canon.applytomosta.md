---
uid: Microsoft.Quantum.Canon.ApplyToMostA
title: Operação ApplyToMostA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostA
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: 7c226de9b2c99d124c467175dfe65a60a89d4332
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208492"
---
# <a name="applytomosta-operation"></a>Operação ApplyToMostA

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma operação a todos, exceto ao último elemento de uma matriz.

```qsharp
operation ApplyToMostA<'T> (op : ('T[] => Unit is Adj), targets : 'T[]) : Unit is Adj
```


## <a name="description"></a>Descrição

Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Most(targets))` .

## <a name="input"></a>Entrada

### <a name="op--t--unit--is-adj"></a>op: ' t [] = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj

Uma operação a ser aplicada.


### <a name="targets--t"></a>destinos: ' t []

Uma matriz de destinos, das quais todos, exceto o último, será aplicado `op` .



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de entrada da operação a ser aplicada.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ApplyToMost](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [Microsoft. Quantum. Canon. ApplyToMostC](xref:Microsoft.Quantum.Canon.ApplyToMostC)
- [Microsoft. Quantum. Canon. ApplyToMostCA](xref:Microsoft.Quantum.Canon.ApplyToMostCA)