---
uid: Microsoft.Quantum.Arrays.Interleaved
title: Função intercalada
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Interleaved
qsharp.summary: Interleaves two arrays of (almost) same size.
ms.openlocfilehash: 8405cabca17f2dd7c2680833bfab5c3768fcf752
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694455"
---
# <a name="interleaved-function"></a>Função intercalada

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Agrupa [](https://nuget.org/packages/)


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