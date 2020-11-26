---
uid: Microsoft.Quantum.Arrays.Where
title: Função Where
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Where
qsharp.summary: Given a predicate and an array, returns the indices of that array where the predicate is true.
ms.openlocfilehash: 97598aa25d2d085aaab94f3d60ee64db9e2b89d6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219916"
---
# <a name="where-function"></a>Função Where

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dado um predicado e uma matriz, retorna os índices dessa matriz em que o predicado é verdadeiro.

```qsharp
function Where<'T> (predicate : ('T -> Bool), array : 'T[]) : Int[]
```


## <a name="input"></a>Entrada

### <a name="predicate--t---bool"></a>predicado: [booliano](xref:microsoft.quantum.lang-ref.bool) -> bool

Uma função de `'T` para booliano que é usada para filtrar elementos.


### <a name="array--t"></a>matriz: ' t []

Uma matriz de elementos `'T` .



## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)[]

Uma matriz de índices em que `predicate` é verdadeira.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de `array` elementos.