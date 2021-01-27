---
uid: Microsoft.Quantum.Arrays.ColumnAt
title: Função ColumnAt
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAt
qsharp.summary: Extracts a column from a matrix.
ms.openlocfilehash: 32dc814de9b04563c2798a768f121723a1a8252c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846265"
---
# <a name="columnat-function"></a>Função ColumnAt

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Extrai uma coluna de uma matriz.

```qsharp
function ColumnAt<'T> (column : Int, matrix : 'T[][]) : 'T[]
```


## <a name="description"></a>Descrição

Essa função extrai uma coluna em uma matriz em ordem de linha.
Extrair uma linha corrsponds para acesso de elemento do primeiro índice e, portanto, não requer tratamento adicional.

## <a name="input"></a>Entrada

### <a name="column--int"></a>coluna: [int](xref:microsoft.quantum.lang-ref.int)

Coluna da matriz


### <a name="matrix--t"></a>matriz: t [] []

matriz 2-dimensional em ordem de linha



## <a name="output--t"></a>Saída: ' T' []



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de cada elemento de `matrix` .

## <a name="example"></a>Exemplo

```qsharp
let matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]];
let column = ColumnAt(0, matrix);
// same as: column = [1, 4, 7]
```

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. arrays. transposed](xref:Microsoft.Quantum.Arrays.Transposed)
- [Microsoft. Quantum. arrays. diagonal](xref:Microsoft.Quantum.Arrays.Diagonal)