---
uid: Microsoft.Quantum.Logical.NotEqualB
title: Função NotEqualB
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualB
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 9f362b9e08f8a798bf7f7d9c323fee6576dccd9f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98814416"
---
# <a name="notequalb-function"></a>Função NotEqualB

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna true se e somente se duas entradas não forem iguais.

```qsharp
function NotEqualB (a : Bool, b : Bool) : Bool
```


## <a name="input"></a>Entrada

### <a name="a--bool"></a>a: [bool](xref:microsoft.quantum.lang-ref.bool)

O primeiro valor a ser comparado.


### <a name="b--bool"></a>b: [bool](xref:microsoft.quantum.lang-ref.bool)

O segundo valor a ser comparado.



## <a name="output--bool"></a>Saída: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` se e somente se `a` não for igual a `b` .

## <a name="remarks"></a>Comentários

Os itens a seguir são equivalentes:

```qsharp
let cond = a != b;
let cond = NotEqualB(a, b);
```