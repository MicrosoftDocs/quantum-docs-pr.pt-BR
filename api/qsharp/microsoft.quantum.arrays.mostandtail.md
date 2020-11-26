---
uid: Microsoft.Quantum.Arrays.MostAndTail
title: Função MostAndTail
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MostAndTail
qsharp.summary: Returns a tuple of all but one and the last element of the array.
ms.openlocfilehash: 392efb20e4aaba80a77664444bb415d8bc9b0930
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220562"
---
# <a name="mostandtail-function"></a>Função MostAndTail

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna uma tupla de todos, exceto um e o último elemento da matriz.

```qsharp
function MostAndTail<'A> (array : 'A[]) : ('A[], 'A)
```


## <a name="input"></a>Entrada

### <a name="array--a"></a>matriz: ' A []

Uma matriz com pelo menos um elemento.



## <a name="output--aa"></a>Saída: (' A [], ' A)

Uma tupla de todos, exceto um e o último elemento da matriz.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="a"></a>' A

O tipo dos elementos da matriz.