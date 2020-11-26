---
uid: Microsoft.Quantum.Preparation.QuantumROM
title: Função QuantumROM
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: QuantumROM
qsharp.summary: >-
  > [!WARNING]

  > QuantumROM has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PurifiedMixedState> instead.


  Uses the Quantum ROM technique to represent a given density matrix.

  Given a list of $N$ coefficients $\alpha_j$, this returns a unitary $U$ that uses the Quantum-ROM technique to prepare an approximation  $\tilde\rho\sum_{j=0}^{N-1}p_j\ket{j}\bra{j}$ of the purification of the density matrix $\rho=\sum_{j=0}^{N-1}\frac{|alpha_j|}{\sum_k |\alpha_k|}\ket{j}\bra{j}$. In this approximation, the error $\epsilon$ is such that $|p_j-\frac{|alpha_j|}{\sum_k |\alpha_k|}|\le \epsilon / N$ and $\|\tilde\rho - \rho\| \le \epsilon$. In other words, $$ \begin{align} U\ket{0}^{\lceil\log_2 N\rceil}\ket{0}^{m}=\sum_{j=0}^{N-1}\sqrt{p_j} \ket{j}\ket{\text{garbage}_j}. \end{align} $$
ms.openlocfilehash: 1ee805fb2ea02121daaab7fc3eb5dbbcb134b470
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229878"
---
# <a name="quantumrom-function"></a>Função QuantumROM

Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


> [!WARNING]
> QuantumROM foi preterido. Use <xref:Microsoft.Quantum.Preparation.PurifiedMixedState> em seu lugar.

Usa a técnica de ROM Quantum para representar uma determinada matriz de densidade.

Dada uma lista de $N $ coeficientes $ \ alpha_j $, isso retorna um $U unitário que usa a técnica Quantum-ROM para preparar uma aproximação $ \tilde\rho\ sum_ {j = 0} ^ {N-1} p_j \ket{j}\bra{j} $ do Purification da matriz de densidade $ \rho = \ sum_ {j = 0} ^ {N-1} \frac{| alpha_j |} {\ sum_k | \ alpha_k |} \ket{j}\bra{j} $. Nessa aproximação, o erro $ \epsilon $ é de que $ | p_j-\frac{| alpha_j |} {\ sum_k | \ alpha_k |} | \le \epsilon/N $ e $ \| \tilde\rho-\rho \| \le \epsilon $. Em outras palavras, $ $ \begin{align} U\ket {0} ^ {\lceil\ Log_2 N\rceil} \ ket {0} ^ {m} = \ sum_ {j = 0} ^ {N-1} \sqrt{p_j} \ket{j}\ket{\Text{Garbage} _J}.
\end{align} $ $

```qsharp
function QuantumROM (targetError : Double, coefficients : Double[]) : ((Int, (Int, Int)), Double, ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl))
```


## <a name="input"></a>Entrada

### <a name="targeterror--double"></a>targetError: [Double](xref:microsoft.quantum.lang-ref.double)

O erro de destino $ \epsilon $.


### <a name="coefficients--double"></a>coeficientes: [duplo](xref:microsoft.quantum.lang-ref.double)[]

Matriz de $N $ coeficientes especificando a probabilidade de Estados de base.
Números negativos $-\ alpha_j $ serão tratados como $ | \ alpha_j | $.



## <a name="output--intintintdoublelittleendianqubit--unit--is-adj--ctl"></a>Saída: (([int](xref:microsoft.quantum.lang-ref.int), ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))),[Double](xref:microsoft.quantum.lang-ref.double), ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL)

## <a name="first-parameter"></a>Primeiro parâmetro

Uma tupla `(x,(y,z))` em que `x = y + z` é o número total de qubits alocadas, `y` é o número de qubits para o `LittleEndian` registro e `z` é o número de qubits de lixo.

## <a name="second-parameter"></a>Segundo parâmetro

A norma One-Activity $ \ sum_j | \ alpha_j | $ da matriz de coeficiente.

## <a name="third-parameter"></a>Terceiro parâmetro

O unitário $U $.

## <a name="references"></a>Referências

- Codificação eletrônica de Spectra em circuitos Quantum com complexidade T linear Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru fosco, Austin Fowler, Hartmut Neven https://arxiv.org/abs/1805.03662