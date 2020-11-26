---
uid: Microsoft.Quantum.Diagnostics.EqualityFactB
title: Função EqualityFactB
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactB
qsharp.summary: Asserts that a classical Bool variable has the expected value.
ms.openlocfilehash: a87d6690e701eb1530be3134d24884a8c19357e9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201913"
---
# <a name="equalityfactb-function"></a>Função EqualityFactB

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Declara que uma variável bool clássica tem o valor esperado.

```qsharp
function EqualityFactB (actual : Bool, expected : Bool, message : String) : Unit
```


## <a name="input"></a>Entrada

### <a name="actual--bool"></a>real: [bool](xref:microsoft.quantum.lang-ref.bool)

A variável a ser verificada.


### <a name="expected--bool"></a>esperado: [bool](xref:microsoft.quantum.lang-ref.bool)

O valor esperado.


### <a name="message--string"></a>mensagem: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)

Cadeia de caracteres de mensagem de falha a ser usada quando a asserção é disparada.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

