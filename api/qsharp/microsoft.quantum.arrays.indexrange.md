---
uid: Microsoft.Quantum.Arrays.IndexRange
title: Função IndexRange
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexRange
qsharp.summary: Given an array, returns a range over the indices of that array, suitable for use in a for loop.
ms.openlocfilehash: 7f9779acd4a781c50388217aa780710bd0b99ff3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694456"
---
# <a name="indexrange-function"></a>Função IndexRange

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Agrupa [](https://nuget.org/packages/)


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