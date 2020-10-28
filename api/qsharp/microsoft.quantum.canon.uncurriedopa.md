---
uid: Microsoft.Quantum.Canon.UncurriedOpA
title: Função UncurriedOpA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `A` indicates that the operations are adjointable.
ms.openlocfilehash: 21df20354ad2388891f32b1bf1c7781287904983
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693872"
---
# <a name="uncurriedopa-function"></a>Função UncurriedOpA

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Agrupa [](https://nuget.org/packages/)


Dada uma função que retorna operações, retorna uma nova operação que usa as duas entradas como uma tupla.
O modificador `A` indica que as operações são adjointable.

```qsharp
function UncurriedOpA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Adj))) : (('T, 'U) => Unit is Adj)
```


## <a name="input"></a>Entrada

### <a name="curriedop--t---u--unit-adj"></a>curriedOp: t-> ' U => adj da [unidade](xref:microsoft.quantum.lang-ref.unit)

Uma função que retorna operações.



## <a name="output--tu--unit-adj"></a>Saída: (' t, ' U) => adj da [unidade](xref:microsoft.quantum.lang-ref.unit)

Uma nova operação `op` , como `op(t, u)` equivalente a `(curriedOp(t))(u)` .

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo do primeiro argumento de uma função na forma curried.
### <a name="u"></a>' U

O tipo do segundo argumento de uma função na forma curried.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. UncurriedOp](xref:Microsoft.Quantum.Canon.UncurriedOp)