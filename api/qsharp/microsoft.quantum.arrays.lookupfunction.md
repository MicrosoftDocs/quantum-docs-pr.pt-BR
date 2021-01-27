---
uid: Microsoft.Quantum.Arrays.LookupFunction
title: Função LookupFunction
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: LookupFunction
qsharp.summary: Given an array, returns a function which returns elements of that array.
ms.openlocfilehash: 22b56bb7e9f03ebc5b2225efb2e6450d56022664
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845694"
---
# <a name="lookupfunction-function"></a>Função LookupFunction

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dada uma matriz, retorna uma função que retorna elementos dessa matriz.

```qsharp
function LookupFunction<'T> (array : 'T[]) : (Int -> 'T)
```


## <a name="input"></a>Entrada

### <a name="array--t"></a>matriz: ' t []

A matriz a ser representada como uma função de pesquisa.



## <a name="output--int---t"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int) -> ' t

Uma função `f` como essa `f(idx) == f[idx]` .

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo dos elementos da matriz que está sendo representada como uma função de pesquisa.

## <a name="remarks"></a>Comentários

Essa função é útil principalmente para interoperar com funções e operações que usam `Int -> 'T` funções como seus argumentos. Isso é comum, por exemplo, na biblioteca de representação do gerador, em que as funções são usadas para evitar a necessidade de registrar uma matriz inteira na memória.