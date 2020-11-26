---
uid: Microsoft.Quantum.Arithmetic.EvaluateOddPolynomialFxP
title: Operação EvaluateOddPolynomialFxP
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluateOddPolynomialFxP
qsharp.summary: Evaluates an odd polynomial in a fixed-point representation.
ms.openlocfilehash: 1bf9b6e7c416e994e70b93e5967caefd444f6426
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223214"
---
# <a name="evaluateoddpolynomialfxp-operation"></a>Operação EvaluateOddPolynomialFxP

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Avalia um polinomial ímpar em uma representação de ponto fixo.

```qsharp
operation EvaluateOddPolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="coefficients--double"></a>coeficientes: [duplo](xref:microsoft.quantum.lang-ref.double)[]

Coeficientes do polinomial estranho como uma matriz dupla, ou seja, a matriz $ [a_0, a_1,..., a_k] $ para a $P polinomial ímpar (x) = a_0 x + a_1 x ^ 3 + \cdots + a_k x ^ {2K + 1} $.


### <a name="fpx--fixedpoint"></a>FPX: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Número de ponto fixo de entrada para o qual avaliar o polinomial.


### <a name="result--fixedpoint"></a>resultado: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

O número de ponto fixo de saída que manterá P (x). Deve estar no estado $ \ket {0} $ inicialmente.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

