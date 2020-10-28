---
uid: Microsoft.Quantum.Arrays.Transposed
title: Função transpoda
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Transposed
qsharp.summary: Returns the transpose of a matrix represented as an array of arrays.
ms.openlocfilehash: 54071c461cf9f9411c332763b81e3bc448fb6c6e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694400"
---
# <a name="transposed-function"></a>Função transpoda

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Agrupa [](https://nuget.org/packages/)


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