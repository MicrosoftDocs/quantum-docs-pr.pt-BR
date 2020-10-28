---
uid: Microsoft.Quantum.Arrays.IndexOf
title: Função IndexOf
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexOf
qsharp.summary: Returns the first index of the first element in an array that satisfies a given predicate. If no such element exists, returns -1.
ms.openlocfilehash: 7ff80f13f432a18f216b2dee4bd65b1e82034fa5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694460"
---
# <a name="indexof-function"></a>Função IndexOf

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Agrupa [](https://nuget.org/packages/)


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

