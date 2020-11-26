---
uid: Microsoft.Quantum.Arithmetic.EvaluatePolynomialFxP
title: Operação EvaluatePolynomialFxP
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluatePolynomialFxP
qsharp.summary: Evaluates a polynomial in a fixed-point representation.
ms.openlocfilehash: 4f6ed4b34af2e63dd8ee31fb9b93119e06e3ecbc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223180"
---
# <a name="evaluatepolynomialfxp-operation"></a>Operação EvaluatePolynomialFxP

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Avalia um polinomial em uma representação de ponto fixo.

```qsharp
operation EvaluatePolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="coefficients--double"></a>coeficientes: [duplo](xref:microsoft.quantum.lang-ref.double)[]

Coeficientes do polinomial como uma matriz Double, ou seja, a matriz $ [a_0, a_1,..., a_d] $ para o polinomial $P (x) = a_0 + a_1 x + \cdots + a_d x ^ d $.


### <a name="fpx--fixedpoint"></a>FPX: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Número de ponto fixo de entrada para o qual avaliar o polinomial.


### <a name="result--fixedpoint"></a>resultado: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

O número de ponto fixo de saída que irá manter $P (x) $. Deve estar no estado $ \ket {0} $ inicialmente.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

