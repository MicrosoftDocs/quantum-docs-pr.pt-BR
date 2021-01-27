---
uid: Microsoft.Quantum.Intrinsic.Message
title: Função de mensagem
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Message
qsharp.summary: Logs a message.
ms.openlocfilehash: 652e33de69ffb725f117db3beeffa66558776f49
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849370"
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