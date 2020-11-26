---
uid: Microsoft.Quantum.Arrays.Filtered
title: Função filtrada
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Filtered
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, returns an array that consists of those elements that satisfy the predicate.
ms.openlocfilehash: fa8600f4d773daf6eabf8b9961ab46961155d1fd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221259"
---
# <a name="filtered-function"></a>Função filtrada

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dada uma matriz e um predicado que é definido para os elementos da matriz, retorna uma matriz que consiste nesses elementos que atendem ao predicado.

```qsharp
function Filtered<'T> (predicate : ('T -> Bool), array : 'T[]) : 'T[]
```


## <a name="input"></a>Entrada

### <a name="predicate--t---bool"></a>predicado: [booliano](xref:microsoft.quantum.lang-ref.bool) -> bool

Uma função de `'T` para booliano que é usada para filtrar elementos.


### <a name="array--t"></a>matriz: ' t []

Uma matriz de elementos `'T` .



## <a name="output--t"></a>Saída: ' T' []

Uma matriz `'T[]` de elementos que satisfazem o predicado.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de `array` elementos.

## <a name="remarks"></a>Comentários

A função é definida para tipos genéricos, ou seja, sempre que temos uma matriz `'T[]` e um predicado, `'T -> Bool` podemos filtrar elementos.