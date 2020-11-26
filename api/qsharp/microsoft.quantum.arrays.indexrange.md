---
uid: Microsoft.Quantum.Arrays.IndexRange
title: Função IndexRange
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexRange
qsharp.summary: Given an array, returns a range over the indices of that array, suitable for use in a for loop.
ms.openlocfilehash: 5afd4cc260ac3e384d2736bf7b43d941afd9ef73
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220936"
---
# <a name="indexrange-function"></a>Função IndexRange

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Dada uma matriz, retorna um intervalo sobre os índices dessa matriz, adequado para uso em um loop for.

```qsharp
function IndexRange<'TElement> (array : 'TElement[]) : Range
```


## <a name="input"></a>Entrada

### <a name="array--telement"></a>matriz: ' TElement []

Uma matriz para a qual um intervalo de índices deve ser retornado.



## <a name="output--range"></a>Saída: [intervalo](xref:microsoft.quantum.lang-ref.range)

Um intervalo em todos os índices da matriz.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="telement"></a>'TElement

O tipo de elementos da matriz.