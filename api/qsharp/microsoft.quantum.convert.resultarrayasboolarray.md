---
uid: Microsoft.Quantum.Convert.ResultArrayAsBoolArray
title: Função ResultArrayAsBoolArray
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: ResultArrayAsBoolArray
qsharp.summary: Converts a `Result[]` type to a `Bool[]` type, where `One` is mapped to `true` and `Zero` is mapped to `false`.
ms.openlocfilehash: 0356fe9c98306ee3e1857f4af311aef9b3789a7d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693606"
---
# <a name="resultarrayasboolarray-function"></a>Função ResultArrayAsBoolArray

Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Agrupa [](https://nuget.org/packages/)


Converte um `Result[]` tipo em um `Bool[]` tipo, onde `One` é mapeado para `true` e `Zero` é mapeado para `false` .

```qsharp
function ResultArrayAsBoolArray (input : Result[]) : Bool[]
```


## <a name="input"></a>Entrada

### <a name="input--__invalidresult__"></a>entrada: __inválido <Result>__ []

`Result[]` a ser convertido.



## <a name="output--bool"></a>Saída: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Um `Bool[]` que representa o `input`.