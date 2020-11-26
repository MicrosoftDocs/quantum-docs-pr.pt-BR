---
uid: Microsoft.Quantum.Diagnostics.EqualityFactCP
title: Função EqualityFactCP
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactCP
qsharp.summary: Asserts that a complex number has the expected value.
ms.openlocfilehash: 39b55e17302f9d2e5049169e9c1a74e53a8b1115
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201845"
---
# <a name="equalityfactcp-function"></a>Função EqualityFactCP

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Declara que um número complexo tem o valor esperado.

```qsharp
function EqualityFactCP (actual : Microsoft.Quantum.Math.ComplexPolar, expected : Microsoft.Quantum.Math.ComplexPolar, message : String) : Unit
```


## <a name="input"></a>Entrada

### <a name="actual--complexpolar"></a>real: [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)

O valor a ser verificado.


### <a name="expected--complexpolar"></a>esperado: [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)

O valor esperado.


### <a name="message--string"></a>mensagem: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)

Cadeia de caracteres de mensagem de falha a ser usada quando a asserção é disparada.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

