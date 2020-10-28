---
uid: Microsoft.Quantum.Logical.Conditioned
title: Função condição
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Conditioned
qsharp.summary: Returns one of two values, depending on the value of a Boolean condition.
ms.openlocfilehash: 8aabe8b018129ddee3b934c207d0a62e59fb6f4a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694729"
---
# <a name="conditioned-function"></a>Função condição

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Agrupa [](https://nuget.org/packages/)


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