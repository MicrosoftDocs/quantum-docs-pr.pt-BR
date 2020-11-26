---
uid: Microsoft.Quantum.Arrays._SwapOrderToPermuteArray
title: Função _SwapOrderToPermuteArray
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: _SwapOrderToPermuteArray
qsharp.summary: Returns the order elements in an array need to be swapped to produce an ordered array. Assumes swaps occur in place.
ms.openlocfilehash: 9df2ec00d91c1124fae960efd15d576b15b0223c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221701"
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

## <a name="remarks"></a>Comentários

## <a name="psuedocode"></a>Psuedocode

para (índice em 0.. Length (newOrder)-1) {enquanto newOrder [index]! = index {switch newOrder [index] with newOrder [newOrder [index]]}}