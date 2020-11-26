---
uid: Microsoft.Quantum.Arrays.Rest
title: Função REST
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Rest
qsharp.summary: Creates an array that is equal to an input array except that the first array element is dropped.
ms.openlocfilehash: 4dd10b6e8839fd906ca9c2e36c89c626d5772149
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220376"
---
# <a name="rest-function"></a>Função REST

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Cria uma matriz que é igual a uma matriz de entrada, exceto que o primeiro elemento da matriz é Descartado.

```qsharp
function Rest<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a>Entrada

### <a name="array--t"></a>matriz: ' t []

Uma matriz cujo segundo para o último elementos é formar a matriz de saída.



## <a name="output--t"></a>Saída: ' T' []

Uma matriz que contém os elementos `array[1..Length(array) - 1]` .

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo dos elementos da matriz.