---
uid: Microsoft.Quantum.Canon.UncurriedOpC
title: Função UncurriedOpC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpC
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `C` indicates that the operations are controllable.
ms.openlocfilehash: 35be5425fcd76eae9e0a6fde6a689a5db00da52f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204582"
---
# <a name="uncurriedopc-function"></a>Função UncurriedOpC

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dada uma função que retorna operações, retorna uma nova operação que usa as duas entradas como uma tupla.
O modificador `C` indica que as operações são controláveis.

```qsharp
function UncurriedOpC<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl))) : (('T, 'U) => Unit is Ctl)
```


## <a name="input"></a>Entrada

### <a name="curriedop--t---u--unit--is-ctl"></a>curriedOp: t-> ' U = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é CTL

Uma função que retorna operações.



## <a name="output--tu--unit--is-ctl"></a>Saída: (' t, ' U) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é CTL

Uma nova operação `op` , como `op(t, u)` equivalente a `(curriedOp(t))(u)` .

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo do primeiro argumento de uma função na forma curried.
### <a name="u"></a>' U

O tipo do segundo argumento de uma função na forma curried.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. UncurriedOp](xref:Microsoft.Quantum.Canon.UncurriedOp)