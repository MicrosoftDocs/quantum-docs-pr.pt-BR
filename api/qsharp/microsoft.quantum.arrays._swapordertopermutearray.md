---
uid: Microsoft.Quantum.Arrays._SwapOrderToPermuteArray
title: Função _SwapOrderToPermuteArray
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: _SwapOrderToPermuteArray
qsharp.summary: Returns the order elements in an array need to be swapped to produce an ordered array. Assumes swaps occur in place.
ms.openlocfilehash: ff8e4e23dde7d69f93054a275548ded49d5b0bfb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846286"
---
# <a name="_swapordertopermutearray-function"></a>Função _SwapOrderToPermuteArray

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna os elementos de ordem em uma matriz que precisam ser trocados para produzir uma matriz ordenada.
Pressupõe que as trocas ocorrem em vigor.

```qsharp
function _SwapOrderToPermuteArray (newOrder : Int[]) : (Int, Int)[]
```


## <a name="input"></a>Entrada

### <a name="neworder--int"></a>newOrder: [int](xref:microsoft.quantum.lang-ref.int)[]

Matriz com a permutação dos índices da nova matriz. Deve haver $n elementos $, cada um com um inteiro exclusivo de $0 $ a $n-$1.



## <a name="output--intint"></a>Saída: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []

A tupla representa os dois índices a serem trocados. As trocas começam no índice mais baixo.

## <a name="example"></a>Exemplo

```qsharp
// The following returns [(0, 5),(0, 4),(0, 1),(0, 3)];
let swapOrder = _SwapOrderToPermuteArray([5, 3, 2, 0, 1, 4]);
```

## <a name="remarks"></a>Comentários

## <a name="psuedocode"></a>Psuedocode

para (índice em 0.. Length (newOrder)-1) {enquanto newOrder [index]! = index {switch newOrder [index] with newOrder [newOrder [index]]}}