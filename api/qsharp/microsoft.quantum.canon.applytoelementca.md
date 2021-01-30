---
uid: Microsoft.Quantum.Canon.ApplyToElementCA
title: Operação ApplyToElementCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElementCA
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: 420a92ae10d2fc260024968b1846e669c4b62d73
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841464"
---
# <a name="applytoelementca-operation"></a>Operação ApplyToElementCA

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma operação a um determinado elemento de uma matriz.

```qsharp
operation ApplyToElementCA<'T> (op : ('T => Unit is Adj + Ctl), index : Int, targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a>Descrição

Dada uma operação `op` , um índice `index` e uma matriz de destinos `targets` , aplicam-se `op(targets[index])` .

## <a name="input"></a>Entrada

### <a name="op--t--unit--is-adj--ctl"></a>op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL

Uma operação a ser aplicada.


### <a name="index--int"></a>índice: [int](xref:microsoft.quantum.lang-ref.int)

Um índice na matriz de destinos.


### <a name="targets--t"></a>destinos: ' t []

Uma matriz de possíveis destinos para `op` .



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de entrada da operação a ser aplicada.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ApplyToElement](xref:Microsoft.Quantum.Canon.ApplyToElement)
- [Microsoft. Quantum. Canon. ApplyToElementC](xref:Microsoft.Quantum.Canon.ApplyToElementC)
- [Microsoft. Quantum. Canon. ApplyToElementA](xref:Microsoft.Quantum.Canon.ApplyToElementA)