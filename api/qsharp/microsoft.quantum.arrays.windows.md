---
uid: Microsoft.Quantum.Arrays.Windows
title: Função do Windows
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Windows
qsharp.summary: Returns all consecutive subarrays of length `size`.
ms.openlocfilehash: 6071d1c3e5981855c57abd0e741b1de0201c30a3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694389"
---
# <a name="windows-function"></a>Função do Windows

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Agrupa [](https://nuget.org/packages/)


Retorna todas as submatrizes consecutivas de comprimento `size` .

```qsharp
function Windows<'T> (size : Int, array : 'T[]) : 'T[][]
```


## <a name="description"></a>Descrição

Essa função retorna todas as `n - size + 1` submatrizes de length `size` em ordem, em que `n` é o comprimento de `arr` .
As primeiras submatrizes são `arr[0..size - 1], arr[1..size], arr[2..size + 1]` até a última submatriz `arr[n - size..n - 1]` .

Se `size <= 0` ou `size > n` , uma matriz vazia será retornada.

## <a name="input"></a>Entrada

### <a name="size--int"></a>Tamanho: [int](xref:microsoft.quantum.lang-ref.int)

Comprimento das submatrizes.


### <a name="array--t"></a>matriz: ' t []

Uma matriz de elementos.



## <a name="output--t"></a>Saída: ' T' [] []



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de `array` elementos.