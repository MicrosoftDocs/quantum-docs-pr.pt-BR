---
uid: Microsoft.Quantum.Convert.ResultArrayAsBoolArray
title: Função ResultArrayAsBoolArray
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: ResultArrayAsBoolArray
qsharp.summary: Converts a `Result[]` type to a `Bool[]` type, where `One` is mapped to `true` and `Zero` is mapped to `false`.
ms.openlocfilehash: f3af3abd4ee58f495d4ea60ec4f21a2690abec1d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224217"
---
# <a name="resultarrayasboolarray-function"></a>Função ResultArrayAsBoolArray

Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Converte um `Result[]` tipo em um `Bool[]` tipo, onde `One` é mapeado para `true` e `Zero` é mapeado para `false` .

```qsharp
function ResultArrayAsBoolArray (input : Result[]) : Bool[]
```


## <a name="input"></a>Entrada

### <a name="input--__invalidresult__"></a>entrada: __inválido <Result>__[]

`Result[]` a ser convertido.



## <a name="output--bool"></a>Saída: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Um `Bool[]` que representa o `input`.