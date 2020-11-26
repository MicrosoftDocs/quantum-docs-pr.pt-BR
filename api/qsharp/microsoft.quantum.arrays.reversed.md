---
uid: Microsoft.Quantum.Arrays.Reversed
title: Função invertida
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Reversed
qsharp.summary: Create an array that contains the same elements as an input array but in Reversed order.
ms.openlocfilehash: 270f15c1d10b4397e258c750876095efc2b8e951
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220426"
---
# <a name="reversed-function"></a>Função invertida

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Crie uma matriz que contenha os mesmos elementos de uma matriz de entrada, mas em ordem inversa.

```qsharp
function Reversed<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a>Entrada

### <a name="array--t"></a>matriz: ' t []

Uma matriz cujos elementos devem ser copiados na ordem inversa.



## <a name="output--t"></a>Saída: ' T' []

Uma matriz que contém os elementos `array[Length(array) - 1]` .. `array[0]`.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo dos elementos da matriz.