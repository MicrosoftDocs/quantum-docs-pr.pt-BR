---
uid: Microsoft.Quantum.Preparation.StatePreparationComplexCoefficients
title: Função StatePreparationComplexCoefficients
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: StatePreparationComplexCoefficients
qsharp.summary: >-
  > [!WARNING]

  > StatePreparationComplexCoefficients has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateCP> instead.


  Returns an operation that prepares a specific quantum state.

  The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0...0}$.

  The action of U on a newly-allocated register is given by $$ \begin{align} U\ket{0...0}=\ket{\psi}=\frac{\sum_{j=0}^{2^n-1}r_j e^{i t_j}\ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|r_j|^2}}. \end{align} $$
ms.openlocfilehash: c16df0fe075b15cff745a6b7d5b79aac39c14d09
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856129"
---
# <a name="statepreparationcomplexcoefficients-function"></a>Função StatePreparationComplexCoefficients

Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


> [!WARNING]
> StatePreparationComplexCoefficients foi preterido. Use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateCP> em seu lugar.

Retorna uma operação que prepara um estado de Quantum específico.

A operação retornada $U $ prepara um estado de Quantum arbitrário $ \ket{\psi} $ com coeficientes complexos $r _j e ^ {i t_j} $ do estado de base computacional do $n $-qubit $ \ket{0...0} $.

A ação de U em um registro recém-alocado é fornecida por $ $ \begin{align} U\ket {0... 0} = \ket{\psi} = \frac{\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \ket{j}}{\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}.
\end{align} $ $

```qsharp
function StatePreparationComplexCoefficients (coefficients : Microsoft.Quantum.Math.ComplexPolar[]) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a>Entrada

### <a name="coefficients--complexpolar"></a>coeficientes: [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]

Matriz de até $2 ^ n $ coeficientes complexos representados por seu valor absoluto e fase $ (r_j, t_j) $. O coeficiente $j $ th indexa o estado de número $ \ket{j} $ codificado em um formato little-endian.



## <a name="output--littleendian--unit--is-adj--ctl"></a>Saída: [](xref:Microsoft.Quantum.Arithmetic.LittleEndian) a => [unidade](xref:microsoft.quantum.lang-ref.unit) LittleEndian é adj + CTL

Uma operação unitário de preparação de estado $U $.

## <a name="example"></a>Exemplo

O trecho a seguir prepara o estado Quantum $ \ket{\psi} = e ^ {i 0,1} \ sqrt {1/8} \ ket {0} + \ sqrt {7/8} \ ket {2} $ no registro qubit `qubitsLE` .

```qsharp
let amplitudes = [Sqrt(0.125), 0.0, Sqrt(0.875), 0.0];
let phases = [0.1, 0.0, 0.0, 0.0];
mutable complexNumbers = new ComplexPolar[4];
for (idx in 0..3) {
    set complexNumbers[idx] = ComplexPolar(amplitudes[idx], phases[idx]);
}
let op = StatePreparationComplexCoefficients(complexNumbers);
using (qubits = Qubit[2]) {
    let qubitsLE = LittleEndian(qubits);
    op(qubitsLE);
}
```

## <a name="remarks"></a>Comentários

Coeficientes de entrada negativas $r _j < $0 serão tratados como se positivo com o valor $ | r_j | $. `coefficients` será preenchido com os elementos $ (r_j, t_j) = (0,0, 0,0) $ se menos de $2 ^ n $ forem especificados.