---
uid: Microsoft.Quantum.Logical.Conditioned
title: Função condição
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Conditioned
qsharp.summary: Returns one of two values, depending on the value of a Boolean condition.
ms.openlocfilehash: c0f55d4db95ad1f0d2b7f291cbc6ba8ae704cb81
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198479"
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

```Q#
let x = condition ? ifTrue | ifFalse;
let x = Conditioned(condition, ifTrue, ifFalse);
```