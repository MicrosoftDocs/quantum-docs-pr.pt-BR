---
uid: Microsoft.Quantum.Arrays.Fold
title: Função de dobra
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Fold
qsharp.summary: Iterates a function `f` through an array `array`, returning `f(f(f(initialState, array[0]), array[1]), ...)`.
ms.openlocfilehash: d12e070058178ce2cbdd70cade5bc16607a55d5e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848598"
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

## <a name="example"></a>Exemplo

```qsharp
function Plus(a : Double, b : Double) {
    return a + b;
}
function Sum(xs : Double[]) {
    return Fold(Plus, 0.0, xs);
}
```