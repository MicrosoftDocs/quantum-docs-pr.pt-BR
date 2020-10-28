---
uid: Microsoft.Quantum.Chemistry.IsNotZero
title: Função IsNotZero
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: IsNotZero
qsharp.summary: Checks whether a `Double` number is not approximately zero.
ms.openlocfilehash: 3c0f9c6695e8c9ec4a0953d5217c28c512ac7de1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693816"
---
# <a name="isnotzero-function"></a>Função IsNotZero

Namespace: [Microsoft. Quantum. química](xref:Microsoft.Quantum.Chemistry)

Agrupa [](https://nuget.org/packages/)


Verifica se um `Double` número não é aproximadamente zero.

```qsharp
function IsNotZero (number : Double) : Bool
```


## <a name="input"></a>Entrada

### <a name="number--double"></a>número: [duplo](xref:microsoft.quantum.lang-ref.double)

Número a ser verificado



## <a name="output--bool"></a>Saída: [bool](xref:microsoft.quantum.lang-ref.bool)

Retornará true se `number` tiver um valor absoluto maior que `1e-15` .