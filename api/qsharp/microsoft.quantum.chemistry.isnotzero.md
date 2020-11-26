---
uid: Microsoft.Quantum.Chemistry.IsNotZero
title: Função IsNotZero
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: IsNotZero
qsharp.summary: Checks whether a `Double` number is not approximately zero.
ms.openlocfilehash: f80dbba6a51e62970e87c2782faba558340d2bd8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204055"
---
# <a name="isnotzero-function"></a>Função IsNotZero

Namespace: [Microsoft. Quantum. química](xref:Microsoft.Quantum.Chemistry)

Pacote: [Microsoft. Quantum. química](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Verifica se um `Double` número não é aproximadamente zero.

```qsharp
function IsNotZero (number : Double) : Bool
```


## <a name="input"></a>Entrada

### <a name="number--double"></a>número: [duplo](xref:microsoft.quantum.lang-ref.double)

Número a ser verificado



## <a name="output--bool"></a>Saída: [bool](xref:microsoft.quantum.lang-ref.bool)

Retornará true se `number` tiver um valor absoluto maior que `1e-15` .