---
uid: Microsoft.Quantum.Diagnostics.EqualityFactI
title: Função EqualityFactI
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactI
qsharp.summary: Asserts that a classical Int variable has the expected value.
ms.openlocfilehash: 27c0642f6d89aaa715526092813240e11b9ab530
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201828"
---
# <a name="equalityfacti-function"></a>Função EqualityFactI

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Declara que uma variável int clássica tem o valor esperado.

```qsharp
function EqualityFactI (actual : Int, expected : Int, message : String) : Unit
```


## <a name="input"></a>Entrada

### <a name="actual--int"></a>real: [int](xref:microsoft.quantum.lang-ref.int)

O número a ser verificado.


### <a name="expected--int"></a>esperado: [int](xref:microsoft.quantum.lang-ref.int)

O valor esperado.


### <a name="message--string"></a>mensagem: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)

Cadeia de caracteres de mensagem de falha a ser usada quando a asserção é disparada.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

