---
uid: Microsoft.Quantum.Arrays.Padded
title: Função preenchida
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Padded
qsharp.summary: Returns an array padded at with specified values up to a specified length.
ms.openlocfilehash: 556e5f5175ee54470a99f32c037eeb2cd80588d0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845556"
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

## <a name="example"></a>Exemplo

```qsharp
let array = [10, 11, 12];
// The following line returns [10, 12, 15, 2, 2, 2].
let output = Padded(-6, array, 2);
// The following line returns [2, 2, 2, 10, 12, 15].
let output = Padded(6, array, 2);
```