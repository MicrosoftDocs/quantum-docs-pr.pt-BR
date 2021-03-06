---
uid: Microsoft.Quantum.Arrays.MappedByIndex
title: Função MappedByIndex
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedByIndex
qsharp.summary: Given an array and a function that is defined for the indexed elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 584cabcb7b6059ae5d311f13f5f75bd1f87bdba5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845659"
---
# <a name="mappedbyindex-function"></a>Função MappedByIndex

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dada uma matriz e uma função que é definida para os elementos indexados da matriz, retorna uma nova matriz que consiste nas imagens da matriz original sob a função.

```qsharp
function MappedByIndex<'T, 'U> (mapper : ((Int, 'T) -> 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a>Entrada

### <a name="mapper--intt---u"></a>mapeador: ([int](xref:microsoft.quantum.lang-ref.int), ' t)-> ' U

Uma função de `(Int, 'T)` para `'U` que é usada para mapear elementos e seus índices.


### <a name="array--t"></a>matriz: ' t []

Uma matriz de elementos `'T` .



## <a name="output--u"></a>Saída: ' U []

Uma matriz `'U[]` de elementos que são mapeados pela `mapper` função.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de `array` elementos.
### <a name="u"></a>' U

O tipo de resultado da `mapper` função.

## <a name="example"></a>Exemplo

As duas linhas a seguir são equivalentes:

```qsharp
let arr = MapIndex(f, [x0, x1, x2]);
```

e

```qsharp
let arr = [f(0, x0), f(1, x1), f(2, x2)];
```

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. arrays. mapeado](xref:Microsoft.Quantum.Arrays.Mapped)