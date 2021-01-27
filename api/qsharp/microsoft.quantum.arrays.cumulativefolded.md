---
uid: Microsoft.Quantum.Arrays.CumulativeFolded
title: Função CumulativeFolded
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: CumulativeFolded
qsharp.summary: Combines Mapped and Fold into a single function
ms.openlocfilehash: 95cd5233a09a1234bba4de9fe870b9d93c0f86a4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846236"
---
# <a name="cumulativefolded-function"></a>Função CumulativeFolded

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Combina mapeadas e dobras em uma única função

```qsharp
function CumulativeFolded<'State, 'T> (fn : (('State, 'T) -> 'State), state : 'State, array : 'T[]) : 'State[]
```


## <a name="description"></a>Descrição

Essa função itera a `fn` função por meio da matriz, começando a partir de um estado inicial `state` e retorna todos os valores intermediários, não incluindo o estado inicial.

## <a name="input"></a>Entrada

### <a name="fn--statet---state"></a>FN: (' State, ' t)-estado de >

Uma função a ser dobrada sobre a matriz


### <a name="state--state"></a>Estado: ' estado

O estado inicial a ser dobrado


### <a name="array--t"></a>matriz: ' t []

Uma matriz de valores a serem dobrados



## <a name="output--state"></a>Saída: ' State []

Todos os Estados intermediários, incluindo o estado final, mas não o estado inicial.
O comprimento da matriz de saída é do mesmo comprimento que `array` .

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="state"></a>' Estado

O tipo de estado no qual a `fn` função Opera, ou seja, aceita como sua primeira entrada e retorna.
### <a name="t"></a>T'

O tipo de `array` elementos.

## <a name="example"></a>Exemplo

```qsharp
// same as sums = [1, 3, 6, 10, 15]
let sums = CumulativeFolded(PlusI, 0, SequenceI(1, 5));
```