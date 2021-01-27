---
uid: Microsoft.Quantum.Convert.ResultArrayAsBoolArray
title: Função ResultArrayAsBoolArray
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: ResultArrayAsBoolArray
qsharp.summary: Converts a `Result[]` type to a `Bool[]` type, where `One` is mapped to `true` and `Zero` is mapped to `false`.
ms.openlocfilehash: 384531137474562ebc8cc24dcd1ac976dc91ad9d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98832586"
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