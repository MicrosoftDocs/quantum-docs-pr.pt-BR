---
uid: Microsoft.Quantum.Canon.UncurriedOpC
title: Função UncurriedOpC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpC
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `C` indicates that the operations are controllable.
ms.openlocfilehash: f3e5ecf3f7df0393dfbb948f064c27505f04cfcf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693871"
---
# <a name="uncurriedopc-function"></a>Função UncurriedOpC

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Agrupa [](https://nuget.org/packages/)


Dada uma função que retorna operações, retorna uma nova operação que usa as duas entradas como uma tupla.
O modificador `C` indica que as operações são controláveis.

```qsharp
function UncurriedOpC<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl))) : (('T, 'U) => Unit is Ctl)
```


## <a name="input"></a>Entrada

### <a name="curriedop--t---u--unit-ctl"></a>curriedOp: t-> ' U = CTL de [unidade](xref:microsoft.quantum.lang-ref.unit) de>

Uma função que retorna operações.



## <a name="output--tu--unit-ctl"></a>Saída: (' t, ' U) => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit)

Uma nova operação `op` , como `op(t, u)` equivalente a `(curriedOp(t))(u)` .

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo do primeiro argumento de uma função na forma curried.
### <a name="u"></a>' U

O tipo do segundo argumento de uma função na forma curried.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. UncurriedOp](xref:Microsoft.Quantum.Canon.UncurriedOp)