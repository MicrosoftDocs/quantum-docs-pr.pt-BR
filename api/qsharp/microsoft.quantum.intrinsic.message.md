---
uid: Microsoft.Quantum.Intrinsic.Message
title: Função de mensagem
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Message
qsharp.summary: Logs a message.
ms.openlocfilehash: 4eb55dd4fd8d78e4b5a9bb289dacfbdb3aa4beb8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96199005"
---
# <a name="message-function"></a>Função de mensagem

Namespace: [Microsoft. Quantum. intrínseco](xref:Microsoft.Quantum.Intrinsic)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Registra uma mensagem.

```qsharp
function Message (msg : String) : Unit
```


## <a name="input"></a>Entrada

### <a name="msg--string"></a>msg: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)

A mensagem a ser relatada.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

O comportamento específico dessa função é dependente de simulador, mas na maioria dos casos a mensagem fornecida será gravada no console.