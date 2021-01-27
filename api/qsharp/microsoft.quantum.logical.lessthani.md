---
uid: Microsoft.Quantum.Logical.LessThanI
title: Função LessThanI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanI
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: 69c3d7c414967b830c15189c895a2b34f409c7b3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98815828"
---
# <a name="lessthani-function"></a>Função LessThanI

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna true se e somente se um número for menor que outro número.

```qsharp
function LessThanI (a : Int, b : Int) : Bool
```


## <a name="input"></a>Entrada

### <a name="a--int"></a>r: [int](xref:microsoft.quantum.lang-ref.int)

O primeiro valor a ser comparado.


### <a name="b--int"></a>b: [int](xref:microsoft.quantum.lang-ref.int)

O segundo valor a ser comparado.



## <a name="output--bool"></a>Saída: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` se e somente se `a` for estritamente menor que `b` .

## <a name="remarks"></a>Comentários

Os itens a seguir são equivalentes:

```qsharp
let cond = a < b;
let cond = LessThanI(a, b);
```