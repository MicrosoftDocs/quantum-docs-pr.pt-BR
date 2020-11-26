---
uid: Microsoft.Quantum.Arrays.Fold
title: Função de dobra
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Fold
qsharp.summary: Iterates a function `f` through an array `array`, returning `f(f(f(initialState, array[0]), array[1]), ...)`.
ms.openlocfilehash: a42f9a832c18bd612c1ae416187f3f2513eed54d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221157"
---
# <a name="fold-function"></a>Função de dobra

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Itera uma função `f` por meio de uma matriz `array` , retornando `f(f(f(initialState, array[0]), array[1]), ...)` .

```qsharp
function Fold<'State, 'T> (folder : (('State, 'T) -> 'State), state : 'State, array : 'T[]) : 'State
```


## <a name="input"></a>Entrada

### <a name="folder--statet---state"></a>pasta: (' State, ' t)-estado de >

Uma função a ser dobrada sobre a matriz.


### <a name="state--state"></a>Estado: ' estado

O estado inicial da pasta.


### <a name="array--t"></a>matriz: ' t []

Uma matriz de valores a serem dobrados.



## <a name="output--state"></a>Saída: ' estado

O estado final retornado pela pasta após a iteração em todos os elementos de `array` .

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="state"></a>' Estado

O tipo de Estados em que a `folder` função Opera, ou seja, aceita como seu primeiro argumento e retorna.
### <a name="t"></a>T'

O tipo de `array` elementos.