---
uid: Microsoft.Quantum.Arrays.Exclude
title: Função Exclude
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Exclude
qsharp.summary: Returns an array containing the elements of another array, excluding elements at a given list of indices.
ms.openlocfilehash: 4ea0d754fce4fc7e3e4e42e55b56720cb3f95ca6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221344"
---
# <a name="exclude-function"></a>Função Exclude

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna uma matriz que contém os elementos de outra matriz, excluindo os elementos em uma determinada lista de índices.

```qsharp
function Exclude<'T> (remove : Int[], array : 'T[]) : 'T[]
```


## <a name="input"></a>Entrada

### <a name="remove--int"></a>remover: [int](xref:microsoft.quantum.lang-ref.int)[]

Uma matriz de índices indicando quais elementos devem ser excluídos da saída.


### <a name="array--t"></a>matriz: ' t []

Matriz da qual os valores na matriz de saída são obtidos.



## <a name="output--t"></a>Saída: ' T' []

Uma matriz `output` que `output[0]` é o primeiro elemento de `array` cujo índice não aparece `remove` , tal como `output[1]` é o segundo elemento, e assim por diante.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo dos elementos da matriz.