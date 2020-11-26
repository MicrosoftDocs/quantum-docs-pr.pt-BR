---
uid: Microsoft.Quantum.Arrays.Transposed
title: Função transpoda
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Transposed
qsharp.summary: Returns the transpose of a matrix represented as an array of arrays.
ms.openlocfilehash: f293399d8e3a2cb32b2929e8d1591ac5eaefd277
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219984"
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