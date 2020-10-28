---
uid: Microsoft.Quantum.Convert.BoolAsResult
title: Função BoolAsResult
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolAsResult
qsharp.summary: Converts a `Bool` type to a `Result` type, where `true` is mapped to `One` and `false` is mapped to `Zero`.
ms.openlocfilehash: eea6c062afdbb3172e63261e52a82e2576c14011
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693639"
---
# <a name="boolasresult-function"></a>Função BoolAsResult

Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Agrupa [](https://nuget.org/packages/)


Converte um `Bool` tipo em um `Result` tipo, onde `true` é mapeado para `One` e `false` é mapeado para `Zero` .

```qsharp
function BoolAsResult (input : Bool) : Result
```


## <a name="input"></a>Entrada

### <a name="input--bool"></a>entrada: [bool](xref:microsoft.quantum.lang-ref.bool)

`Bool` a ser convertido.



## <a name="output--__invalidresult__"></a>Saída: __inválida <Result>__

Um `Result` que representa o `input`.