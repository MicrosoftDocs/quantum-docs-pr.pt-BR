---
uid: Microsoft.Quantum.Canon.OperationPowC
title: Função OperationPowC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowC
qsharp.summary: >-
  Raises an operation to a power. The modifier `C` indicates that the operation is controllable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 05b0d5b286e16c308d8c3df8fb8fa1ac8c9868ca
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852343"
---
# <a name="operationpowc-function"></a>Função OperationPowC

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gera uma operação para uma potência.
O modificador `C` indica que a operação é controlável.

Ou seja, dada uma operação que representa um portão $U $, retorna uma nova operação $U ^ m $ para um Power $m $.

```qsharp
function OperationPowC<'T> (op : ('T => Unit is Ctl), power : Int) : ('T => Unit is Ctl)
```


## <a name="input"></a>Entrada

### <a name="op--t--unit--is-ctl"></a>op: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é CTL

Uma operação $U $ que representa o portão a ser repetido.


### <a name="power--int"></a>potência: [int](xref:microsoft.quantum.lang-ref.int)

O número de vezes que $U $ será repetido.



## <a name="output--t--unit--is-ctl"></a>Saída: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é CTL

Uma nova operação representando $U ^ m $, em que $m = \texttt{Power} $.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo da operação a ser alimentada.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. OperationPow](xref:Microsoft.Quantum.Canon.OperationPow)