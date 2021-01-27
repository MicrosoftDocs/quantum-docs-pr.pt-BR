---
uid: Microsoft.Quantum.Arrays.Chunks
title: Função de partes
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Chunks
qsharp.summary: Splits an array into multiple parts of equal length.
ms.openlocfilehash: 977594839a7d2fe09de8138d32a4a50e8a752390
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842885"
---
# <a name="chunks-function"></a>Função de partes

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Divide uma matriz em várias partes de comprimento igual.

```qsharp
function Chunks<'T> (nElements : Int, arr : 'T[]) : 'T[][]
```


## <a name="input"></a>Entrada

### <a name="nelements--int"></a>nElements: [int](xref:microsoft.quantum.lang-ref.int)

O comprimento de cada parte.


### <a name="arr--t"></a>arr: ' t []

A matriz a ser dividida.



## <a name="output--t"></a>Saída: ' T' [] []

Uma matriz que contém cada parte da matriz original.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'



## <a name="remarks"></a>Comentários

Observe que o último elemento da saída pode ser menor do que `nElements` se `Length(arr)` não for divisível pelo `nElements` .