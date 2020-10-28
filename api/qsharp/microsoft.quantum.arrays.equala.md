---
uid: Microsoft.Quantum.Arrays.EqualA
title: Função equala
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: EqualA
qsharp.summary: Given two arrays of the same type and a predicate that is defined for pairs of elements of the arrays, checks whether the arrays are equal.
ms.openlocfilehash: 24fd76aaeb66081d6d8f1eaa3056117f54b5a5e7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694479"
---
# <a name="equala-function"></a>Função equala

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Agrupa [](https://nuget.org/packages/)


Dadas duas matrizes do mesmo tipo e um predicado que é definido para pares de elementos das matrizes, verifica se as matrizes são iguais.

```qsharp
function EqualA<'T> (equal : (('T, 'T) -> Bool), array1 : 'T[], array2 : 'T[]) : Bool
```


## <a name="input"></a>Entrada

### <a name="equal--tt---bool"></a>igual: (não, não)-> [bool](xref:microsoft.quantum.lang-ref.bool)

Uma função de tupla `('T, 'T)` para `Bool` que é usada para verificar se dois elementos de matrizes são iguais.


### <a name="array1--t"></a>matriz1: ' t []

A primeira matriz a ser comparada.


### <a name="array2--t"></a>matriz2: ' t []

A segunda matriz a ser comparada.



## <a name="output--bool"></a>Saída: [bool](xref:microsoft.quantum.lang-ref.bool)

O valor `true` se e somente se `array1` e `array2` forem iguais.
Ou seja, se ambas as matrizes tiverem o mesmo comprimento e todos os elementos forem iguais, conforme definido pelo `equal` .

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo dos elementos de cada matriz.

## <a name="remarks"></a>Comentários

Essa função é definida para tipos genéricos; ou seja, sempre que tivermos duas matrizes `'T[]` e uma função `equal: ('T, 'T) -> Bool` , essa função retornará um `Bool` valor que indica se as matrizes são iguais.
Para que duas matrizes sejam consideradas iguais, elas precisam ter comprimento igual e os elementos nas mesmas posições nas matrizes devem ser iguais.