---
uid: Microsoft.Quantum.Logical.LessThanOrEqualL
title: Função LessThanOrEqualL
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanOrEqualL
qsharp.summary: Returns true if and only if a number is less than or equal to another number.
ms.openlocfilehash: 1de3fdb0fa53fef9cbf4b9ee9b6a1c54865bd093
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849107"
---
# <a name="lessthanorequall-function"></a>Função LessThanOrEqualL

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retornará true se e somente se um número for menor ou igual a outro número.

```qsharp
function LessThanOrEqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a>Entrada

### <a name="a--bigint"></a>a: [bigint](xref:microsoft.quantum.lang-ref.bigint)

O primeiro valor a ser comparado.


### <a name="b--bigint"></a>b: [bigint](xref:microsoft.quantum.lang-ref.bigint)

O segundo valor a ser comparado.



## <a name="output--bool"></a>Saída: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` se e somente se `a` for menor ou igual a `b` .

## <a name="remarks"></a>Comentários

Os itens a seguir são equivalentes:

```qsharp
let cond = a <= b;
let cond = LessThanOrEqualL(a, b);
```