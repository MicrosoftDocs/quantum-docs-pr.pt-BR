---
uid: Microsoft.Quantum.Arithmetic.MultiplyFxP
title: Operação MultiplyFxP
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyFxP
qsharp.summary: Multiplies two fixed-point numbers in quantum registers.
ms.openlocfilehash: 3c9ef9ade660e1f420d85162104d773b96722eeb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222602"
---
# <a name="multiplyfxp-operation"></a>Operação MultiplyFxP

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Multiplica dois números de ponto fixo em registros de Quantum.

```qsharp
operation MultiplyFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="fp1--fixedpoint"></a>FP1: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Primeiro número de ponto fixo.


### <a name="fp2--fixedpoint"></a>FP2: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Segundo número de ponto fixo.


### <a name="result--fixedpoint"></a>resultado: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Resultado número de ponto fixo, deve estar no estado $ \ket {0} $ inicialmente.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

A implementação atual requer que os três números de ponto fixo tenham a mesma posição de ponto e o mesmo número de qubits.