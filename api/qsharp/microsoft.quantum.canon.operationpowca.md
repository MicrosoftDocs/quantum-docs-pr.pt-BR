---
uid: Microsoft.Quantum.Canon.OperationPowCA
title: Função OperationPowCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowCA
qsharp.summary: >-
  Raises an operation to a power. The modifier `A` indicates that the operation is controllable and adjointable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 753063452616747309e3e228ce8a702f4378c61f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693937"
---
# <a name="operationpowca-function"></a>Função OperationPowCA

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Agrupa [](https://nuget.org/packages/)


Gera uma operação para uma potência.
O modificador `A` indica que a operação é controlável e de adjointable.

Ou seja, dada uma operação que representa um portão $U $, retorna uma nova operação $U ^ m $ para um Power $m $.

```qsharp
function OperationPowCA<'T> (op : ('T => Unit is Ctl + Adj), power : Int) : ('T => Unit is Ctl + Adj)
```


## <a name="input"></a>Entrada

### <a name="op--t--unit-ctl--adj"></a>op: ' t => da [unidade](xref:microsoft.quantum.lang-ref.unit) CTL + adj

Uma operação $U $ que representa o portão a ser repetido.


### <a name="power--int"></a>potência: [int](xref:microsoft.quantum.lang-ref.int)

O número de vezes que $U $ será repetido.



## <a name="output--t--unit-ctl--adj"></a>Saída: t => da [unidade](xref:microsoft.quantum.lang-ref.unit) CTL + adj

Uma nova operação representando $U ^ m $, em que $m = \texttt{Power} $.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo da operação a ser alimentada.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. OperationPow](xref:Microsoft.Quantum.Canon.OperationPow)