---
uid: Microsoft.Quantum.Arrays.Mapped
title: Função mapeada
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Mapped
qsharp.summary: Given an array and a function that is defined for the elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 00ea0803faf6e8edfa748af63dd6c7e217b1de41
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845683"
---
# <a name="mapped-function"></a>Função mapeada

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dada uma matriz e uma função que é definida para os elementos da matriz, retorna uma nova matriz que consiste nas imagens da matriz original sob a função.

```qsharp
function Mapped<'T, 'U> (mapper : ('T -> 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a>Entrada

### <a name="mapper--t---u"></a>mapeador: t-> ' U

Uma função de `'T` para `'U` que é usada para mapear elementos.


### <a name="array--t"></a>matriz: ' t []

Uma matriz de elementos `'T` .



## <a name="output--u"></a>Saída: ' U []

Uma matriz `'U[]` de elementos que são mapeados pela `mapper` função.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de `array` elementos.
### <a name="u"></a>' U

O tipo de resultado da `mapper` função.

## <a name="remarks"></a>Comentários

A função é definida para tipos genéricos, ou seja, sempre que temos uma matriz `'T[]` e uma função, `mapper: 'T -> 'U` podemos mapear os elementos da matriz e produzir uma nova matriz do tipo `'U[]` .