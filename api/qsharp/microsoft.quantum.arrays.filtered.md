---
uid: Microsoft.Quantum.Arrays.Filtered
title: Função filtrada
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Filtered
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, returns an array that consists of those elements that satisfy the predicate.
ms.openlocfilehash: 83336b7001ce1d8ab1f5340b194abdcf93588c31
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847156"
---
# <a name="filtered-function"></a>Função filtrada

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dada uma matriz e um predicado que é definido para os elementos da matriz, retorna uma matriz que consiste nesses elementos que atendem ao predicado.

```qsharp
function Filtered<'T> (predicate : ('T -> Bool), array : 'T[]) : 'T[]
```


## <a name="input"></a>Entrada

### <a name="predicate--t---bool"></a>predicado: [booliano](xref:microsoft.quantum.lang-ref.bool) -> bool

Uma função de `'T` para booliano que é usada para filtrar elementos.


### <a name="array--t"></a>matriz: ' t []

Uma matriz de elementos `'T` .



## <a name="output--t"></a>Saída: ' T' []

Uma matriz `'T[]` de elementos que satisfazem o predicado.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de `array` elementos.

## <a name="example"></a>Exemplo

O código a seguir demonstra a função "Filtered".
Um predicado é definido usando a @"microsoft.quantum.logical.greaterthani" função:

```qsharp
open Microsoft.Quantum.Arrays;
open Microsoft.Quantum.Logical;

function FilteredDemo() : Unit {
   let predicate = GreaterThanI(_, 5);
   let filteredArray = Filtered(predicate, [2, 5, 9, 1, 8]);
   Message($"{filteredArray}");
}
```

O resultado que um deve esperar deste exemplo será uma matriz de números maior que 5.

## <a name="remarks"></a>Comentários

A função é definida para tipos genéricos, ou seja, sempre que temos uma matriz `'T[]` e um predicado, `'T -> Bool` podemos filtrar elementos.