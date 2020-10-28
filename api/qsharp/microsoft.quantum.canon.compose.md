---
uid: Microsoft.Quantum.Canon.Compose
title: Função compor
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Compose
qsharp.summary: Returns the composition of two functions.
ms.openlocfilehash: 02cff7eef4d55d27d5d72e6219a90b7d8f5beb3b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694054"
---
# <a name="compose-function"></a>Função compor

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Agrupa [](https://nuget.org/packages/)


Retorna a composição de duas funções.

```qsharp
function Compose<'T, 'U, 'V> (outer : ('U -> 'V), inner : ('T -> 'U)) : ('T -> 'V)
```


## <a name="description"></a>Descrição

Dadas duas funções $f $ e $g $, retorna uma nova função representando $f \circ g $.

## <a name="input"></a>Entrada

### <a name="outer--u---v"></a>externo: ' U-> ' V

A segunda função a ser aplicada.


### <a name="inner--t---u"></a>interno: ' t-> ' U

A primeira função a ser aplicada.



## <a name="output--t---v"></a>Saída: ' t-> ' V

Uma nova função $h $ de modo que para todas as entradas $x $, $f (g (x)) = h (x) $.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de entrada da primeira função a ser aplicada.
### <a name="u"></a>' U

O tipo de saída da primeira função a ser aplicada e o tipo de entrada da segunda função a ser aplicada.
### <a name="v"></a>' V

O tipo de saída da segunda função a ser aplicada.