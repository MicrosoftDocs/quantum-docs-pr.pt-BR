---
uid: Microsoft.Quantum.Logical.EqualL
title: Função de igual
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualL
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 395b8fedd3b3334939c2a4b5602ee19e0c6e34b0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198105"
---
# <a name="equall-function"></a>Função de igual

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna true se e somente se duas entradas forem iguais.

```qsharp
function EqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a>Entrada

### <a name="a--bigint"></a>a: [bigint](xref:microsoft.quantum.lang-ref.bigint)

O primeiro valor a ser comparado.


### <a name="b--bigint"></a>b: [bigint](xref:microsoft.quantum.lang-ref.bigint)

O segundo valor a ser comparado.



## <a name="output--bool"></a>Saída: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` se e somente se `a` for igual a `b` .

## <a name="remarks"></a>Comentários

Os itens a seguir são equivalentes:

```Q#
let cond = a == b;
let cond = EqualL(a, b);
```