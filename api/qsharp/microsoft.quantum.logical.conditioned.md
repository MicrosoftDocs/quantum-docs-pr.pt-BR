---
uid: Microsoft.Quantum.Logical.Conditioned
title: Função condição
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Conditioned
qsharp.summary: Returns one of two values, depending on the value of a Boolean condition.
ms.openlocfilehash: ea3b8eba960acceb6540978c6fccd9f796b0f67d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98817294"
---
# <a name="conditioned-function"></a>Função condição

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna um dos dois valores, dependendo do valor de uma condição booliana.

```qsharp
function Conditioned<'T> (condition : Bool, ifTrue : 'T, ifFalse : 'T) : 'T
```


## <a name="input"></a>Entrada

### <a name="condition--bool"></a>condição: [bool](xref:microsoft.quantum.lang-ref.bool)

Uma condição usada para controlar qual entrada é retornada.


### <a name="iftrue--t"></a>ifTrue: ' t

O valor a ser retornado quando `condition` for `true` .


### <a name="iffalse--t"></a>ifFalse: ' t

O valor a ser retornado quando `condition` for `false` .



## <a name="output--t"></a>Saída: ' t

`ifTrue` Se `condition` for `true` , e `ifFalse` caso contrário.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'



## <a name="remarks"></a>Comentários

Ao contrário do `?|` operador, essa função não é de curto circuito, de modo que ambas as entradas são totalmente avaliadas.

Até o comportamento de curto-circuito, os seguintes são equivalentes:

```qsharp
let x = condition ? ifTrue | ifFalse;
let x = Conditioned(condition, ifTrue, ifFalse);
```