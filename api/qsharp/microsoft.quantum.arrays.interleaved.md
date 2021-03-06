---
uid: Microsoft.Quantum.Arrays.Interleaved
title: Função intercalada
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Interleaved
qsharp.summary: Interleaves two arrays of (almost) same size.
ms.openlocfilehash: 3605c0d0bc43cdb1097d025861c3ec2424763c86
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848107"
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

## <a name="example"></a>Exemplo

```qsharp
// same as int1 = [1, -1, 2, -2, 3, -3]
let int1 = Interleaved([1, 2, 3], [-1, -2, -3])

// same as int2 = [false, true, false, true, false]
let int2 = Interleaved(ConstantArray(3, false), ConstantArray(2, true));
```