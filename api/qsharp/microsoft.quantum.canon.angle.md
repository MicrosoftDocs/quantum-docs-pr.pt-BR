---
uid: Microsoft.Quantum.Canon.Angle
title: Função Angle
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Angle
qsharp.summary: Returns 1, if `index` has an odd number of 1s and -1, if `index` has an even number of 1s.
ms.openlocfilehash: da3ecdaf1b2c88180bd2a660fac0b6e87b2cafa1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694346"
---
# <a name="angle-function"></a>Função Angle

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Agrupa [](https://nuget.org/packages/)


Retornará 1, se `index` tiver um número ímpar de 1s e-1, se `index` tiver um número par de 1s.

```qsharp
function Angle (index : Int) : Int
```


## <a name="description"></a>Descrição

O valor corresponde ao sinal do coeficiente do Rademacher-Walsh espectro da variável n e da função para uma determinada Atribuição que decide o ângulo da rotação.

## <a name="input"></a>Entrada

### <a name="index--int"></a>índice: [int](xref:microsoft.quantum.lang-ref.int)

Atribuição de entrada como um inteiro (de 0 a 2 ^ n-1)



## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)

