---
uid: Microsoft.Quantum.Math.ArgComplex
title: Função ArgComplex
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ArgComplex
qsharp.summary: Returns the phase of a complex number of type `Complex`.
ms.openlocfilehash: 259296f397207cde4a7d6dfe6cfb1a18e8055216
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211093"
---
# <a name="argcomplex-function"></a>Função ArgComplex

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna a fase de um número complexo de tipo `Complex` .

```qsharp
function ArgComplex (input : Microsoft.Quantum.Math.Complex) : Double
```


## <a name="input"></a>Entrada

### <a name="input--complex"></a>entrada: [complexo](xref:Microsoft.Quantum.Math.Complex)

Número complexo $c = x + i y $.



## <a name="output--double"></a>Saída: [duplo](xref:microsoft.quantum.lang-ref.double)

Fase $ \text{Arg} [c] = \text{ArcTan} (y, x) na (-\pi, \pi] $.