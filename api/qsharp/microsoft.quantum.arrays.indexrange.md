---
uid: Microsoft.Quantum.Arrays.IndexRange
title: Função IndexRange
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexRange
qsharp.summary: Given an array, returns a range over the indices of that array, suitable for use in a for loop.
ms.openlocfilehash: 043b56a1ac3cbe5cd59cdd45d3725f301d81a6ee
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845791"
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

## <a name="example"></a>Exemplo

Os seguintes `for` loops são equivalentes:

```qsharp
for (idx in IndexRange(array)) { ... }
for (idx in IndexRange(array)) { ... }
```