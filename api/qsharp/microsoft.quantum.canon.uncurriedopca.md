---
uid: Microsoft.Quantum.Canon.UncurriedOpCA
title: Função UncurriedOpCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpCA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `CA` indicates that the operations are controllable and adjointable.
ms.openlocfilehash: 6a0f2e1b345d0ba3ac5c779c5dc2bfffaf659a0b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693870"
---
# <a name="uncurriedopca-function"></a>Função UncurriedOpCA

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Agrupa [](https://nuget.org/packages/)


Dada uma função que retorna operações, retorna uma nova operação que usa as duas entradas como uma tupla.
O modificador `CA` indica que as operações são controláveis e adjointable.

```qsharp
function UncurriedOpCA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl + Adj))) : (('T, 'U) => Unit is Ctl + Adj)
```


## <a name="input"></a>Entrada

### <a name="curriedop--t---u--unit-ctl--adj"></a>curriedOp: t-> ' U => da [unidade](xref:microsoft.quantum.lang-ref.unit) CTL + adj

Uma função que retorna operações.



## <a name="output--tu--unit-ctl--adj"></a>Saída: (' t, ' U) => [unidade](xref:microsoft.quantum.lang-ref.unit) CTL + adj

Uma nova operação `op` , como `op(t, u)` equivalente a `(curriedOp(t))(u)` .

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo do primeiro argumento de uma função na forma curried.
### <a name="u"></a>' U

O tipo do segundo argumento de uma função na forma curried.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. UncurriedOp](xref:Microsoft.Quantum.Canon.UncurriedOp)