---
uid: Microsoft.Quantum.Math.AbsComplex
title: Função AbsComplex
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: AbsComplex
qsharp.summary: Returns the absolute value of a complex number of type `Complex`.
ms.openlocfilehash: 2bb4caa140bef36d893da834eac1c94b8dd8b0e2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846079"
---
# <a name="abscomplex-function"></a>Função AbsComplex

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna o valor absoluto de um número complexo de tipo `Complex` .

```qsharp
function AbsComplex (input : Microsoft.Quantum.Math.Complex) : Double
```


## <a name="input"></a>Entrada

### <a name="input--complex"></a>entrada: [complexo](xref:Microsoft.Quantum.Math.Complex)

Número complexo $c = x + i y $.



## <a name="output--double"></a>Saída: [duplo](xref:microsoft.quantum.lang-ref.double)

Valor absoluto $ | c | = \sqrt{x ^ 2 + y ^ 2} $.