---
uid: Microsoft.Quantum.Convert.BoolAsResult
title: Função BoolAsResult
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolAsResult
qsharp.summary: Converts a `Bool` type to a `Result` type, where `true` is mapped to `One` and `false` is mapped to `Zero`.
ms.openlocfilehash: 0190529dd804922a69499fbf1c2c4c916c4b720a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214238"
---
# <a name="boolasresult-function"></a>Função BoolAsResult

Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Converte um `Bool` tipo em um `Result` tipo, onde `true` é mapeado para `One` e `false` é mapeado para `Zero` .

```qsharp
function BoolAsResult (input : Bool) : Result
```


## <a name="input"></a>Entrada

### <a name="input--bool"></a>entrada: [bool](xref:microsoft.quantum.lang-ref.bool)

`Bool` a ser convertido.



## <a name="output--__invalidresult__"></a>Saída: __inválida <Result>__

Um `Result` que representa o `input`.