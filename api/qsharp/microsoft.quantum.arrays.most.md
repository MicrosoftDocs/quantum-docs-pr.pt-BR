---
uid: Microsoft.Quantum.Arrays.Most
title: A maioria das funções
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Most
qsharp.summary: Creates an array that is equal to an input array except that the last array element is dropped.
ms.openlocfilehash: ca89041a4e70472e9bf7a63ffcacccb35aad527c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694431"
---
# <a name="most-function"></a>A maioria das funções

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Agrupa [](https://nuget.org/packages/)


Cria uma matriz que é igual a uma matriz de entrada, exceto que o último elemento da matriz é Descartado.

```qsharp
function Most<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a>Entrada

### <a name="array--t"></a>matriz: ' t []

Uma matriz cujos primeiros aos últimos elementos são formar a matriz de saída.



## <a name="output--t"></a>Saída: ' T' []

Uma matriz que contém os elementos `array[0..Length(array) - 2]` .

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo dos elementos da matriz.