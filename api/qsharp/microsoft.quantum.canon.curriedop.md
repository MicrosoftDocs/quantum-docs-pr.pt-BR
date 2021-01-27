---
uid: Microsoft.Quantum.Canon.CurriedOp
title: Função CurriedOp
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CurriedOp
qsharp.summary: >-
  Returns a curried version of an operation on two inputs.

  That is, given an operation with two inputs, this function applies Curry's isomorphism $f(x, y) \equiv f(x)(y)$ to return an operation of one input which returns an operation of one input.
ms.openlocfilehash: f811347d65a6460690163e9df631979c906bd89f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840775"
---
# <a name="curriedop-function"></a>Função CurriedOp

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna uma versão na forma curried de uma operação em duas entradas.

Ou seja, dada uma operação com duas entradas, essa função aplica curry isomorphism $f (x, y) \equiv f (x) (y) $ para retornar uma operação de uma entrada que retorna uma operação de uma entrada.

```qsharp
function CurriedOp<'T, 'U> (op : (('T, 'U) => Unit)) : ('T -> ('U => Unit))
```


## <a name="input"></a>Entrada

### <a name="op--tu--unit"></a>op: (' t, ' U) = [unidade](xref:microsoft.quantum.lang-ref.unit) de> 

Uma operação cuja entrada é um par.



## <a name="output--t---u--unit"></a>Saída: t-> ' U = [unidade](xref:microsoft.quantum.lang-ref.unit) de> 

Uma operação que aceita o primeiro elemento de um par e retorna uma operação que aceita como entrada o segundo elemento da entrada da operação original.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo do primeiro componente de uma função definida em pares.
### <a name="u"></a>' U

O tipo do segundo componente de uma função definida em pares.

## <a name="remarks"></a>Comentários

Os itens a seguir são equivalentes:

```qsharp
op(x, y);

let curried = CurriedOp(op);
let partial = curried(x);
partial(y);
```