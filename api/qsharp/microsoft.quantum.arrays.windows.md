---
uid: Microsoft.Quantum.Arrays.Windows
title: Função do Windows
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Windows
qsharp.summary: Returns all consecutive subarrays of length `size`.
ms.openlocfilehash: adfea2b9a2f6c22446817538d29586284dba723e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842206"
---
# <a name="windows-function"></a>Função do Windows

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

## <a name="example"></a>Exemplo

```qsharp
// same as [[1, 2, 3], [2, 3, 4], [3, 4, 5]]
let windows = Windows(3, [1, 2, 3, 4, 5]);
```