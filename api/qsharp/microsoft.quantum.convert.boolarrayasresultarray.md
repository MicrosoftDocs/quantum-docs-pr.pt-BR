---
uid: Microsoft.Quantum.Convert.BoolArrayAsResultArray
title: Função BoolArrayAsResultArray
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsResultArray
qsharp.summary: Converts a `Bool[]` type to a `Result[]` type, where `true` is mapped to `One` and `false` is mapped to `Zero`.
ms.openlocfilehash: 50a2bdb4a73ef9d67d3f5532493c142bb7f753cf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693640"
---
# <a name="boolarrayasresultarray-function"></a>Função BoolArrayAsResultArray

Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Agrupa [](https://nuget.org/packages/)


Converte um `Bool[]` tipo em um `Result[]` tipo, onde `true` é mapeado para `One` e `false` é mapeado para `Zero` .

```qsharp
function BoolArrayAsResultArray (input : Bool[]) : Result[]
```


## <a name="input"></a>Entrada

### <a name="input--bool"></a>entrada: [bool](xref:microsoft.quantum.lang-ref.bool)[]

`Bool[]` a ser convertido.



## <a name="output--__invalidresult__"></a>Saída: __inválido <Result>__ []

Um `Result[]` que representa o `input`.