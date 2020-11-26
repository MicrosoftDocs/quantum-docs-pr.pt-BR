---
uid: Microsoft.Quantum.Arrays.IndexOf
title: Função IndexOf
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexOf
qsharp.summary: Returns the first index of the first element in an array that satisfies a given predicate. If no such element exists, returns -1.
ms.openlocfilehash: d63b204334611f8f2c3860f9ee1d756f637780e2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221004"
---
# <a name="indexof-function"></a>Função IndexOf

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna o primeiro índice do primeiro elemento em uma matriz que atende a um determinado predicado. Se nenhum elemento desse tipo existir, retornará-1.

```qsharp
function IndexOf<'T> (predicate : ('T -> Bool), arr : 'T[]) : Int
```


## <a name="input"></a>Entrada

### <a name="predicate--t---bool"></a>predicado: [booliano](xref:microsoft.quantum.lang-ref.bool) -> bool

Uma função de predicado agindo em elementos da matriz.


### <a name="arr--t"></a>arr: ' t []

Uma matriz a ser pesquisada usando o predicado fornecido.



## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)

O menor índice `idx` , como `predicate(arr[idx])` true, ou-1, se nenhum elemento desse tipo existir.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

