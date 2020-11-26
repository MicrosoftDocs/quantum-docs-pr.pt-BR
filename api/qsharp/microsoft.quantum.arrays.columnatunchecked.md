---
uid: Microsoft.Quantum.Arrays.ColumnAtUnchecked
title: Função ColumnAtUnchecked
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAtUnchecked
qsharp.summary: This function does not check for matrix shape
ms.openlocfilehash: 06fce23bbf7142ee0e0b0ed3f2c0578676f2097b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221582"
---
# <a name="columnatunchecked-function"></a>Função ColumnAtUnchecked

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Esta função não verifica a forma de matriz

```qsharp
function ColumnAtUnchecked<'T> (column : Int, matrix : 'T[][]) : 'T[]
```


## <a name="description"></a>Descrição

Essa função pode ser usada em outras funções multidimensionais, que já verificam a matriz de entrada em busca de uma forma retangular válida.

## <a name="input"></a>Entrada

### <a name="column--int"></a>coluna: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="matrix--t"></a>matriz: t [] []





## <a name="output--t"></a>Saída: ' T' []



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

