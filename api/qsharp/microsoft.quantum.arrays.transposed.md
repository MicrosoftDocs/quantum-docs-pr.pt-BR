---
uid: Microsoft.Quantum.Arrays.Transposed
title: Função transpoda
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Transposed
qsharp.summary: Returns the transpose of a matrix represented as an array of arrays.
ms.openlocfilehash: 913f1829ef53ec3eb6944be8b8e3eb37b431f27e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850927"
---
# <a name="transposed-function"></a>Função transpoda

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna a transpoção de uma matriz representada como uma matriz de matrizes.

```qsharp
function Transposed<'T> (matrix : 'T[][]) : 'T[][]
```


## <a name="description"></a>Descrição

Entrada como um $r \times c $ Matrix com $r $ Rows e $c $ Columns.  A matriz é baseada em linha, ou seja, `matrix[i][j]` acessa o elemento na linha $i $ e coluna $j $.

Essa função retorna o $c \times r $ Matrix que é a transpoção da matriz de entrada.

## <a name="input"></a>Entrada

### <a name="matrix--t"></a>matriz: t [] []

\Times com base em linha $r c $ Matrix



## <a name="output--t"></a>Saída: ' T' [] []

\Times transposed $c r $ Matrix

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de cada elemento de `matrix` .

## <a name="example"></a>Exemplo

```qsharp
// same as [[1, 4], [2, 5], [3, 6]]
let transposed = Transposed([[1, 2, 3], [4, 5, 6]]);
```