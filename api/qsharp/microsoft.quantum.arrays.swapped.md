---
uid: Microsoft.Quantum.Arrays.Swapped
title: Função permutada
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Swapped
qsharp.summary: Applies a swap of two elements in an array.
ms.openlocfilehash: 173fb32b5a41ce054f19548a7fcca18c11c4c4cd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220120"
---
# <a name="swapped-function"></a>Função permutada

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma troca de dois elementos em uma matriz.

```qsharp
function Swapped<'T> (firstIndex : Int, secondIndex : Int, arr : 'T[]) : 'T[]
```


## <a name="input"></a>Entrada

### <a name="firstindex--int"></a>firstIndex: [int](xref:microsoft.quantum.lang-ref.int)

Índice do primeiro elemento a ser trocado.


### <a name="secondindex--int"></a>secondIndex: [int](xref:microsoft.quantum.lang-ref.int)

Índice do segundo elemento a ser trocado.


### <a name="arr--t"></a>arr: ' t []

Matriz com elementos a serem trocados.



## <a name="output--t"></a>Saída: ' T' []

A matriz com a permuta in loco aplicada.

## <a name="example"></a>Exemplo

```qsharp
// The following returns [0, 3, 2, 1, 4]
Swapped(1, 3, [0, 1, 2, 3, 4]);
```

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

