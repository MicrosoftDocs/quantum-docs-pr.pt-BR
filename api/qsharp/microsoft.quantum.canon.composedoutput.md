---
uid: Microsoft.Quantum.Canon.ComposedOutput
title: Função ComposedOutput
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ComposedOutput
qsharp.summary: Returns the output of the composition of `inner` and `outer` for a given input.
ms.openlocfilehash: d39fcd6b2987b3a4f69df13fa83b69a199d6eddb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840883"
---
# <a name="composedoutput-function"></a>Função ComposedOutput

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna a saída da composição de `inner` e `outer` para uma determinada entrada.

```qsharp
function ComposedOutput<'T, 'U, 'V> (outer : ('U -> 'V), inner : ('T -> 'U), target : 'T) : 'V
```


## <a name="input"></a>Entrada

### <a name="outer--u---v"></a>externo: ' U-> ' V




### <a name="inner--t---u"></a>interno: ' t-> ' U




### <a name="target--t"></a>destino: ' t





## <a name="output--v"></a>Saída: ' V



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'


### <a name="u"></a>' U


### <a name="v"></a>' V

