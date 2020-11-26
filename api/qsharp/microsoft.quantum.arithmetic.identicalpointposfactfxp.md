---
uid: Microsoft.Quantum.Arithmetic.IdenticalPointPosFactFxP
title: Função IdenticalPointPosFactFxP
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IdenticalPointPosFactFxP
qsharp.summary: Assert that all fixed-point numbers in the provided array have identical point positions when counting from the least- significant bit. I.e., number of bits minus point position must be constant for all fixed-point numbers in the array.
ms.openlocfilehash: 907e270e1c3710fb346044ad7757171c6d5f568d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223044"
---
# <a name="identicalpointposfactfxp-function"></a>Função IdenticalPointPosFactFxP

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Declare que todos os números de ponto fixo na matriz fornecida têm posições de ponto idênticas ao contar do bit menos significativo. Ou seja, o número de bits e a posição do ponto de menos deve ser constante para todos os números de ponto fixo na matriz.

```qsharp
function IdenticalPointPosFactFxP (fixedPoints : Microsoft.Quantum.Arithmetic.FixedPoint[]) : Unit
```


## <a name="input"></a>Entrada

### <a name="fixedpoints--fixedpoint"></a>fixedPoints: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)[]

Matriz de números de ponto fixo Quantum que serão verificados quanto à compatibilidade (usando asserções).



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

