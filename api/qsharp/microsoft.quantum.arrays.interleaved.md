---
uid: Microsoft.Quantum.Arrays.Interleaved
title: Função intercalada
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Interleaved
qsharp.summary: Interleaves two arrays of (almost) same size.
ms.openlocfilehash: 1ff5999cc19f47e3dcae601b960446923b613d90
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220953"
---
# <a name="interleaved-function"></a>Função intercalada

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Intercala duas matrizes de (quase) mesmo tamanho.

```qsharp
function Interleaved<'T> (first : 'T[], second : 'T[]) : 'T[]
```


## <a name="description"></a>Descrição

Essa função retorna a intercalação de duas matrizes, começando com o primeiro elemento da primeira matriz, depois o primeiro elemento da segunda matriz e assim por diante.

A primeira matriz deve ser do mesmo comprimento que a segunda, ou pode ter mais um elemento.

## <a name="input"></a>Entrada

### <a name="first--t"></a>Primeiro: ' t []

A primeira matriz a ser intercalada.


### <a name="second--t"></a>Segundo: ' t []

A segunda matriz a ser intercalada.



## <a name="output--t"></a>Saída: ' T' []

Matriz intercalada

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de cada elemento de `first` e `second` .