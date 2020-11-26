---
uid: Microsoft.Quantum.Logical.EqualB
title: Função EqualB
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualB
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: b566f5ba8548eadeecf63a1e91956d936e7e9a20
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198462"
---
# <a name="equalb-function"></a>Função EqualB

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna true se e somente se duas entradas forem iguais.

```qsharp
function EqualB (a : Bool, b : Bool) : Bool
```


## <a name="input"></a>Entrada

### <a name="a--bool"></a>a: [bool](xref:microsoft.quantum.lang-ref.bool)

O primeiro valor a ser comparado.


### <a name="b--bool"></a>b: [bool](xref:microsoft.quantum.lang-ref.bool)

O segundo valor a ser comparado.



## <a name="output--bool"></a>Saída: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` se e somente se `a` for igual a `b` .

## <a name="remarks"></a>Comentários

Os itens a seguir são equivalentes:

```Q#
let cond = a == b;
let cond = EqualB(a, b);
```