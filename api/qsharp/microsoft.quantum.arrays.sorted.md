---
uid: Microsoft.Quantum.Arrays.Sorted
title: Função classificada
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Sorted
qsharp.summary: Given an array, returns the elements of that array sorted by a given comparison function.
ms.openlocfilehash: bd8b869e03c7f4687c456a944e07a811ae0d2ce2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220222"
---
# <a name="sorted-function"></a>Função classificada

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dada uma matriz, retorna os elementos dessa matriz classificados por uma determinada função de comparação.

```qsharp
function Sorted<'T> (comparison : (('T, 'T) -> Bool), array : 'T[]) : 'T[]
```


## <a name="input"></a>Entrada

### <a name="comparison--tt---bool"></a>comparação: (não, não)-> [bool](xref:microsoft.quantum.lang-ref.bool)

Uma função que compara dois elementos, de modo que `a` é considerado menor ou igual a `b` se `comparison(a, b)` for `true` .


### <a name="array--t"></a>matriz: ' t []

A matriz a ser classificada.



## <a name="output--t"></a>Saída: ' T' []



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de cada elemento de `array` .

## <a name="remarks"></a>Comentários

Presume- `comparison` se que a função seja transitiva, de modo que, se `comparison(a, b)` e `comparison(b, c)` , `comparison(a, c)` for assumido. Se essa propriedade não for mantida, a saída dessa função poderá estar incorreta.

Como se trata de uma função, os resultados são completamente determinísticass, mesmo quando dois elementos são considerados iguais em `comparison` ; ou seja, quando `comparison(a, b)` e `comparison(b, a)` são ambos `true` .
Em particular, a classificação executada por essa função é garantida como estável, de modo que, se dois elementos `a` e `b` ocorrer nessa ordem dentro `array` e sejam considerados iguais em `comparison` , `a` também aparecerão antes `b` na saída.

Por exemplo:

```Q#
function LastDigitLessThanOrEqual(left : Int, right : Int) : Bool {
    return LessThanOrEqualI(
        left % 10, right % 10
    );
}

function SortedByLastDigit() : Int[] {
    return Sorted(LastDigitLessThanOrEqual, [3, 37, 11, 17]);
}
// returns [11, 3, 37, 17].
```