---
uid: Microsoft.Quantum.Arrays.TupleArrayAsNestedArray
title: Função TupleArrayAsNestedArray
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: TupleArrayAsNestedArray
qsharp.summary: Turns a list of 2-tuples into a nested array.
ms.openlocfilehash: c898178b6385b27f753509f0748a8b666b5066bd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220069"
---
# <a name="tuplearrayasnestedarray-function"></a>Função TupleArrayAsNestedArray

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Transforma uma lista de duas tuplas em uma matriz aninhada.

```qsharp
function TupleArrayAsNestedArray<'T> (tupleList : ('T, 'T)[]) : 'T[][]
```


## <a name="input"></a>Entrada

### <a name="tuplelist--tt"></a>tuplelist: (t, ' t) []

Lista de 2 tuplas a serem transformadas em uma matriz aninhada.



## <a name="output--t"></a>Saída: ' T' [] []

Uma matriz aninhada com comprimento correspondente à tuplalist.

## <a name="example"></a>Exemplo

```qsharp
// The following returns [[2, 3], [4, 5]]
TupleArrayAsNestedArray([(2, 3), (4, 5)]);
```

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

