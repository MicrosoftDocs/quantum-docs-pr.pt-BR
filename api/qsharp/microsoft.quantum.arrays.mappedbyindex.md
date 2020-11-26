---
uid: Microsoft.Quantum.Arrays.MappedByIndex
title: Função MappedByIndex
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedByIndex
qsharp.summary: Given an array and a function that is defined for the indexed elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 430495517974b641c249fa146aa9effec542e825
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209920"
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

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. arrays. mapeado](xref:Microsoft.Quantum.Arrays.Mapped)