---
uid: Microsoft.Quantum.Canon.Snd
title: Função SND
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Snd
qsharp.summary: Given a pair, returns its second element.
ms.openlocfilehash: c05053b45d24c3398526d1269b90bb40d1e0ef27
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693905"
---
# <a name="snd-function"></a>Função SND

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Agrupa [](https://nuget.org/packages/)


Dado um par, retorna seu segundo elemento.

```qsharp
function Snd<'T, 'U> (pair : ('T, 'U)) : 'U
```


## <a name="input"></a>Entrada

### <a name="pair--tu"></a>par: (t, ' U)

Uma tupla com dois elementos.



## <a name="output--u"></a>Saída: ' U

O segundo elemento de `pair` .

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo do primeiro membro do par.
### <a name="u"></a>' U

O tipo do segundo membro do par.