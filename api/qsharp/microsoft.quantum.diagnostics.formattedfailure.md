---
uid: Microsoft.Quantum.Diagnostics.FormattedFailure
title: Função FormattedFailure
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: FormattedFailure
qsharp.summary: Internal function used to fail with meaningful error messages.
ms.openlocfilehash: 6b1202c8897d67e3089a88a0855c8008b3a8c2ba
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98828270"
---
# <a name="formattedfailure-function"></a>Função FormattedFailure

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Função interna usada para falhar com mensagens de erro significativas.

```qsharp
function FormattedFailure<'T> (actual : 'T, expected : 'T, message : String) : Unit
```


## <a name="input"></a>Entrada

### <a name="actual--t"></a>real: ' t




### <a name="expected--t"></a>esperado: ' t




### <a name="message--string"></a>mensagem: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)





## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'



## <a name="remarks"></a>Comentários

Essa função deve ser emulada por tempos de execução de simulação, para permitir o encaminhamento de contradição formatadas.