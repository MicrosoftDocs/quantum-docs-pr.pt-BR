---
uid: Microsoft.Quantum.Arithmetic.EvaluateEvenPolynomialFxP
title: Operação EvaluateEvenPolynomialFxP
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluateEvenPolynomialFxP
qsharp.summary: Evaluates an even polynomial in a fixed-point representation.
ms.openlocfilehash: 21c700ccb2b87b906fc4d8b65eddf962353948c1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223248"
---
# <a name="evaluateevenpolynomialfxp-operation"></a>Operação EvaluateEvenPolynomialFxP

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Avalia um mesmo polinomial em uma representação de ponto fixo.

```qsharp
operation EvaluateEvenPolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="coefficients--double"></a>coeficientes: [duplo](xref:microsoft.quantum.lang-ref.double)[]

Coeficientes do mesmo polinomial como uma matriz Double, ou seja, a matriz $ [a_0, a_1,..., a_k] $ para o $P polinomial (x) = a_0 + a_1 x ^ 2 + \cdots + a_k x ^ {2K} $.


### <a name="fpx--fixedpoint"></a>FPX: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Número de ponto fixo de entrada para o qual avaliar o polinomial.


### <a name="result--fixedpoint"></a>resultado: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

O número de ponto fixo de saída que irá manter $P (x) $. Deve estar no estado $ \ket {0} $ inicialmente.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

