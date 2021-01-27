---
uid: Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryStateD
title: Operação ApproximatelyPrepareArbitraryStateD
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: ApproximatelyPrepareArbitraryStateD
qsharp.summary: Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients, up to a given approximation tolerance.
ms.openlocfilehash: a818ada509bcb34682ac1230eb508f0b71b5d019
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842459"
---
# <a name="approximatelypreparearbitrarystated-operation"></a>Operação ApproximatelyPrepareArbitraryStateD

Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dado um conjunto de coeficientes e um registro de Quantum codificado little-endian, o prepara um estado nesse registro descrito pelos coeficientes fornecidos, até uma determinada tolerância a uma aproximação.

```qsharp
operation ApproximatelyPrepareArbitraryStateD (tolerance : Double, coefficients : Double[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Descrição

Esta operação prepara um estado de Quantum arbitrário $ \ket{\psi} $ com coeficientes complexos $r _j e ^ {i t_j} $ do estado base computacional $n $-qubit $ \ket{0 \cdots 0} $.
Em particular, a ação dessa operação pode ser simulada pela transformação unitário $U $, que age no estado todos-zeros como

$ $ \begin{align} U\ket {0... 0} & = \ket{\psi} \\ \\ & = \frac{\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \ket{j}} {\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}.
\end{align} $ $

## <a name="input"></a>Entrada

### <a name="tolerance--double"></a>tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)

A tolerância de aproximação a ser usada ao preparar o estado fornecido.


### <a name="coefficients--double"></a>coeficientes: [duplo](xref:microsoft.quantum.lang-ref.double)[]

Matriz de até US $2 ^ n $ reais coeficientes. O coeficiente $j $ th indexa o estado de número $ \ket{j} $ codificado em um formato little-endian.


### <a name="qubits--littleendian"></a>qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Qubit registra os Estados de número de codificação no formato little-endian. Isso deve ser inicializado no estado de base computacional $ \ket{0...0} $.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

Coeficientes de entrada negativas $r _j < $0 serão tratados como se positivo com o valor $ | r_j | $. `coefficients` será preenchido com os elementos $ (r_j, t_j) = (0,0, 0,0) $ se menos de $2 ^ n $ forem especificados.

## <a name="references"></a>Referências

- Síntese de circuitos lógicos Quantum Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176