---
uid: Microsoft.Quantum.Canon.OperationPowC
title: Função OperationPowC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowC
qsharp.summary: >-
  Raises an operation to a power. The modifier `C` indicates that the operation is controllable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: f3c51410fb7c091385b64a1c4c99b3972d5055b1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693939"
---
# <a name="operationpowc-function"></a>Função OperationPowC

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Agrupa [](https://nuget.org/packages/)


Gera uma operação para uma potência.
O modificador `C` indica que a operação é controlável.

Ou seja, dada uma operação que representa um portão $U $, retorna uma nova operação $U ^ m $ para um Power $m $.

```qsharp
function OperationPowC<'T> (op : ('T => Unit is Ctl), power : Int) : ('T => Unit is Ctl)
```


## <a name="input"></a>Entrada

### <a name="op--t--unit-ctl"></a>op: ' t => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit)

Uma operação $U $ que representa o portão a ser repetido.


### <a name="power--int"></a>potência: [int](xref:microsoft.quantum.lang-ref.int)

O número de vezes que $U $ será repetido.



## <a name="output--t--unit-ctl"></a>Saída: t => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit)

Uma nova operação representando $U ^ m $, em que $m = \texttt{Power} $.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo da operação a ser alimentada.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. OperationPow](xref:Microsoft.Quantum.Canon.OperationPow)