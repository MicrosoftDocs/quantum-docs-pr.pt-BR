---
uid: Microsoft.Quantum.Logical.And
title: Função and
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: And
qsharp.summary: Returns the Boolean conjunction of two values.
ms.openlocfilehash: 6c405bdb4182cc7f32bd04952dec25a974c03445
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849238"
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

```qsharp
let x = a and b;
let x = And(a, b);
```