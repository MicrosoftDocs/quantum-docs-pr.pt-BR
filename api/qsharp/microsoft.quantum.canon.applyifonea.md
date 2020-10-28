---
uid: Microsoft.Quantum.Canon.ApplyIfOneA
title: Operação ApplyIfOneA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOneA
qsharp.summary: Applies an adjointable operation conditioned on a classical result value being one.
ms.openlocfilehash: 76c15aba6042c2801ecfe8470e82099c54ba3846
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694283"
---
# <a name="applyifonea-operation"></a>Operação ApplyIfOneA

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Agrupa [](https://nuget.org/packages/)


Aplica uma operação de modo adjacente condição em um valor de resultado clássico sendo um.

```qsharp
operation ApplyIfOneA<'T> (result : Result, (op : ('T => Unit is Adj), target : 'T)) : Unit
```


## <a name="description"></a>Descrição

Dada uma operação `op` e um valor de resultado `result` , aplica- `op` `target` se ao If `result` is `One` . Se `Zero` nada acontecer com o `target` .
O sufixo `A` indica que a operação a ser aplicada é adjointable.

## <a name="input"></a>Entrada

### <a name="result--__invalidresult__"></a>resultado: __inválido <Result>__

Um resultado de medida que controla se op é aplicado ou não.


### <a name="op--t--unit-adj"></a>op: ' t => adj de [unidade](xref:microsoft.quantum.lang-ref.unit)

Uma operação a ser aplicada condicionalmente.


### <a name="target--t"></a>destino: ' t

A entrada à qual a operação é aplicada.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de entrada da operação a ser aplicada condicionalmente.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ApplyIfOneC](xref:Microsoft.Quantum.Canon.ApplyIfOneC)
- [Microsoft. Quantum. Canon. ApplyIfOneA](xref:Microsoft.Quantum.Canon.ApplyIfOneA)
- [Microsoft. Quantum. Canon. ApplyIfOneCA](xref:Microsoft.Quantum.Canon.ApplyIfOneCA)