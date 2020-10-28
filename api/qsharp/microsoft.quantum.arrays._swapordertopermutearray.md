---
uid: Microsoft.Quantum.Arrays._SwapOrderToPermuteArray
title: Função _SwapOrderToPermuteArray
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: _SwapOrderToPermuteArray
qsharp.summary: Returns the order elements in an array need to be swapped to produce an ordered array. Assumes swaps occur in place.
ms.openlocfilehash: 965f2f3d4f8b366abb27287ce0d27a3b7d7b8fb8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694513"
---
# <a name="_swapordertopermutearray-function"></a>Função _SwapOrderToPermuteArray

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Agrupa [](https://nuget.org/packages/)


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

## <a name="remarks"></a>Comentários

## <a name="psuedocode"></a>Psuedocode

para (índice em 0.. Length (newOrder)-1) {enquanto newOrder [index]! = index {switch newOrder [index] with newOrder [newOrder [index]]}}