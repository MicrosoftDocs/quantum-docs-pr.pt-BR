---
uid: Microsoft.Quantum.Logical.And
title: Função and
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: And
qsharp.summary: Returns the Boolean conjunction of two values.
ms.openlocfilehash: 279221ed785dd76e28146e4c22e70290936bf529
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198564"
---
# <a name="and-function"></a>Função and

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna a conjunção booliana de dois valores.

```qsharp
function And (a : Bool, b : Bool) : Bool
```


## <a name="input"></a>Entrada

### <a name="a--bool"></a>a: [bool](xref:microsoft.quantum.lang-ref.bool)

O primeiro valor a ser considerado.


### <a name="b--bool"></a>b: [bool](xref:microsoft.quantum.lang-ref.bool)

O segundo valor a ser considerado.



## <a name="output--bool"></a>Saída: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` se e somente se `a` e `b` forem ambos `true` .

## <a name="remarks"></a>Comentários

Ao contrário do `and` operador, essa função não é de curto circuito, de modo que ambas as entradas são totalmente avaliadas.

Até o comportamento de curto-circuito, os seguintes são equivalentes:

```Q#
let x = a and b;
let x = And(a, b);
```