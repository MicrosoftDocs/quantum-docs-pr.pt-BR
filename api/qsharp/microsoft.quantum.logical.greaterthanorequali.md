---
uid: Microsoft.Quantum.Logical.GreaterThanOrEqualI
title: Função GreaterThanOrEqualI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanOrEqualI
qsharp.summary: Returns true if and only if a number is greater than or equal to another number.
ms.openlocfilehash: 292599c18d2aac44cef8f0eecca38eb1fbe22061
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696808"
---
# <a name="greaterthanorequali-function"></a>Função GreaterThanOrEqualI

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Agrupa [](https://nuget.org/packages/)


Retorna true se e somente se um número for maior ou igual a outro número.

```qsharp
function GreaterThanOrEqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a>Entrada

### <a name="a--int"></a>r: [int](xref:microsoft.quantum.lang-ref.int)

O primeiro valor a ser comparado.


### <a name="b--int"></a>b: [int](xref:microsoft.quantum.lang-ref.int)

O segundo valor a ser comparado.



## <a name="output--bool"></a>Saída: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` se e somente se `a` for maior que ou for igual a `b` .

## <a name="remarks"></a>Comentários

Os itens a seguir são equivalentes:

```Q#
let cond = a >= b;
let cond = GreaterThanOrEqualI(a, b);
```