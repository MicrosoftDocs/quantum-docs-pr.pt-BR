---
uid: Microsoft.Quantum.Arrays.IndexOf
title: Função IndexOf
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexOf
qsharp.summary: Returns the first index of the first element in an array that satisfies a given predicate. If no such element exists, returns -1.
ms.openlocfilehash: 64db55e831078a7130a3ced6a30bfbd2299c392d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848519"
---
# <a name="indexof-function"></a>Função IndexOf

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna o primeiro índice do primeiro elemento em uma matriz que atende a um determinado predicado. Se nenhum elemento desse tipo existir, retornará-1.

```qsharp
function IndexOf<'T> (predicate : ('T -> Bool), arr : 'T[]) : Int
```


## <a name="input"></a>Entrada

### <a name="predicate--t---bool"></a>predicado: [booliano](xref:microsoft.quantum.lang-ref.bool) -> bool

Uma função de predicado agindo em elementos da matriz.


### <a name="arr--t"></a>arr: ' t []

Uma matriz a ser pesquisada usando o predicado fornecido.



## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)

O menor índice `idx` , como `predicate(arr[idx])` true, ou-1, se nenhum elemento desse tipo existir.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'



## <a name="example"></a>Exemplo

Suponha que `IsEven : Int -> Bool` seja uma função que retorna `true` se e somente se sua entrada for par. Em seguida, isso pode ser usado com `IndexOf` para localizar o primeiro elemento par em uma matriz:

```qsharp
let items = [1, 3, 17, 2, 21];
let idx = IndexOf(IsEven, items); // returns 3
```