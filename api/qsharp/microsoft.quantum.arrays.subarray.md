---
uid: Microsoft.Quantum.Arrays.Subarray
title: Função de submatriz
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Subarray
qsharp.summary: Takes an array and a list of locations and produces a new array formed from the elements of the original array that match the given locations.
ms.openlocfilehash: cf72f04421b277ce64354d1eccec11cbc61d78cc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220154"
---
# <a name="subarray-function"></a>Função de submatriz

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Usa uma matriz e uma lista de locais e produz uma nova matriz formada a partir dos elementos da matriz original que correspondem aos locais determinados.

```qsharp
function Subarray<'T> (indices : Int[], array : 'T[]) : 'T[]
```


## <a name="input"></a>Entrada

### <a name="indices--int"></a>índices: [int](xref:microsoft.quantum.lang-ref.int)[]

Uma lista de inteiros que é usada para definir a submatriz.


### <a name="array--t"></a>matriz: ' t []

Uma matriz de elementos `'T` .



## <a name="output--t"></a>Saída: ' T' []

Uma matriz `out` de elementos cujos índices correspondem à submatriz, assim `out[idx] == array[indices[idx]]` .

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de `array` elementos.

## <a name="remarks"></a>Comentários

A função é definida para tipos genéricos, ou seja, sempre que temos uma matriz `'T[]` e uma lista de locais que `Int[]` definem a submatriz.
A construção da submatriz é baseada na geração de uma nova cópia profunda da matriz especificada, em oposição à manutenção de referências.

Se `Length(indices) < Length(array)` , essa função retornará um subconjunto de `array` . Por outro lado, se `indices` contiver elementos repetidos, os elementos correspondentes do `array` serão repetidos da mesma forma.
Se `indices` e `array` tiverem o mesmo comprimento, essa função fornecerá permutações de `array` .