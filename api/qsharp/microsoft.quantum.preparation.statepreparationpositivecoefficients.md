---
uid: Microsoft.Quantum.Preparation.StatePreparationPositiveCoefficients
title: Função StatePreparationPositiveCoefficients
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: StatePreparationPositiveCoefficients
qsharp.summary: >-
  > [!WARNING]

  > StatePreparationPositiveCoefficients has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateD> instead.


  Returns an operation that prepares the given quantum state.

  The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with positive coefficients $\alpha_j\ge 0$ from the $n$-qubit computational basis state $\ket{0...0}$.

  The action of U on a newly-allocated register is given by $$ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\sum_{j=0}^{2^n-1}\alpha_j \ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|\alpha_j|^2}}. \end{align} $$
ms.openlocfilehash: 081541d93bf853fa0de1573038dc00c296432281
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855855"
---
# <a name="statepreparationpositivecoefficients-function"></a>Função StatePreparationPositiveCoefficients

Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


> [!WARNING]
> StatePreparationPositiveCoefficients foi preterido. Use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateD> em seu lugar.

Retorna uma operação que prepara o estado de Quantum fornecido.

A operação retornada $U $ prepara um estado de Quantum arbitrário $ \ket{\psi} $ com coeficientes positivos $ \ alpha_j \ge $0 do estado de base computacional $n $-qubit $ \ket{0...0} $.

A ação de U em um registro recém-alocado é fornecida por $ $ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\ sum_ {j = 0} ^ {2 ^ n-1} \ alpha_j \ket{j}}{\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | \ alpha_j | ^ 2}}.
\end{align} $ $

```qsharp
function StatePreparationPositiveCoefficients (coefficients : Double[]) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a>Entrada

### <a name="coefficients--double"></a>coeficientes: [duplo](xref:microsoft.quantum.lang-ref.double)[]

Matriz de até $2 ^ n $ coeficientes $ \ alpha_j $. O coeficiente $j $ th indexa o estado de número $ \ket{j} $ codificado em um formato little-endian.



## <a name="output--littleendian--unit--is-adj--ctl"></a>Saída: [](xref:Microsoft.Quantum.Arithmetic.LittleEndian) a => [unidade](xref:microsoft.quantum.lang-ref.unit) LittleEndian é adj + CTL

Uma operação unitário de preparação de estado $U $.

## <a name="example"></a>Exemplo

O trecho a seguir prepara o estado Quantum $ \ket{\psi} = \ sqrt {1/8} \ ket {0} + \ sqrt {7/8} \ ket {2} $ no registro qubit `qubitsLE` .

```qsharp
let amplitudes = [Sqrt(0.125), 0.0, Sqrt(0.875), 0.0];
let op = StatePreparationPositiveCoefficients(amplitudes);
using (qubits = Qubit[2]) {
    let qubitsLE = LittleEndian(qubits);
    op(qubitsLE);
}
```

## <a name="remarks"></a>Comentários

Os coeficientes de entrada negativos $ \ alpha_j < $0 serão tratados como se positivo com o valor $ | \ alpha_j | $. `coefficients` será preenchido com os elementos $ \ alpha_j = $0 se menos de $2 ^ n $ forem especificados.