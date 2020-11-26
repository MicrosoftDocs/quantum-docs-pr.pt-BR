---
uid: Microsoft.Quantum.Diagnostics.EqualityFactL
title: Função EqualityFactL
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactL
qsharp.summary: Asserts that a classical BigInt variable has the expected value.
ms.openlocfilehash: 2aaabf39d6ce49952466a877685776490ef438ad
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201794"
---
# <a name="equalityfactl-function"></a>Função EqualityFactL

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Declara que uma variável BigInt clássica tem o valor esperado.

```qsharp
function EqualityFactL (actual : BigInt, expected : BigInt, message : String) : Unit
```


## <a name="input"></a>Entrada

### <a name="actual--bigint"></a>real: [bigint](xref:microsoft.quantum.lang-ref.bigint)

O número a ser verificado.


### <a name="expected--bigint"></a>esperado: [bigint](xref:microsoft.quantum.lang-ref.bigint)

O valor esperado.


### <a name="message--string"></a>mensagem: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)

Cadeia de caracteres de mensagem de falha a ser usada quando a asserção é disparada.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

