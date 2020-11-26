---
uid: Microsoft.Quantum.Arrays.ColumnAt
title: Função ColumnAt
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAt
qsharp.summary: Extracts a column from a matrix.
ms.openlocfilehash: 097b3fdd6fc1843ada27052fcf08ee80d894d25a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210090"
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

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. arrays. transposed](xref:Microsoft.Quantum.Arrays.Transposed)
- [Microsoft. Quantum. arrays. diagonal](xref:Microsoft.Quantum.Arrays.Diagonal)