---
uid: Microsoft.Quantum.Logical.GreaterThanL
title: Função GreaterThanL
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanL
qsharp.summary: Returns true if and only if a number is greater than another number.
ms.openlocfilehash: 5e1b2adab36b7937c83ea912b8a9cb148b626ee5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197969"
---
# <a name="greaterthanl-function"></a>Função GreaterThanL

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna true se e somente se um número for maior que outro número.

```qsharp
function GreaterThanL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a>Entrada

### <a name="a--bigint"></a>a: [bigint](xref:microsoft.quantum.lang-ref.bigint)

O primeiro valor a ser comparado.


### <a name="b--bigint"></a>b: [bigint](xref:microsoft.quantum.lang-ref.bigint)

O segundo valor a ser comparado.



## <a name="output--bool"></a>Saída: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` se e somente se `a` for estritamente maior que `b` .

## <a name="remarks"></a>Comentários

Os itens a seguir são equivalentes:

```Q#
let cond = a > b;
let cond = GreaterThanL(a, b);
```