---
uid: Microsoft.Quantum.Arrays.Padded
title: Função preenchida
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Padded
qsharp.summary: Returns an array padded at with specified values up to a specified length.
ms.openlocfilehash: 2b7a80d1cf5c82a1ff52bc4aa207cfe335b40061
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220528"
---
# <a name="padded-function"></a>Função preenchida

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna uma matriz preenchida com valores especificados até um comprimento especificado.

```qsharp
function Padded<'T> (nElementsTotal : Int, defaultElement : 'T, inputArray : 'T[]) : 'T[]
```


## <a name="input"></a>Entrada

### <a name="nelementstotal--int"></a>nElementsTotal: [int](xref:microsoft.quantum.lang-ref.int)

O comprimento da matriz preenchida. Se isso for positivo, `inputArray` será preenchido no cabeçalho. Se isso for negativo, `inputArray` será preenchido na parte final.


### <a name="defaultelement--t"></a>padrão: ' t

Valor padrão a ser usado para elementos de preenchimento.


### <a name="inputarray--t"></a>inputArray: ' t []

Matriz cujos valores estão no início da matriz de saída.



## <a name="output--t"></a>Saída: ' T' []

Uma matriz `output` que é `inputArray` preenchida na cabeça com `defaultElement` s até o `output` comprimento `nElementsTotal`

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo dos elementos da matriz.