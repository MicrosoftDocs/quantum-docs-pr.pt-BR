---
uid: Microsoft.Quantum.Arrays.Chunks
title: Função de partes
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Chunks
qsharp.summary: Splits an array into multiple parts of equal length.
ms.openlocfilehash: fe10999d35ed05908fd59b9dad8b5c0c51233ae6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694509"
---
# <a name="chunks-function"></a>Função de partes

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Agrupa [](https://nuget.org/packages/)


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