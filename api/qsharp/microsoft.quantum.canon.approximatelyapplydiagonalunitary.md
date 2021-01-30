---
uid: Microsoft.Quantum.Canon.ApproximatelyApplyDiagonalUnitary
title: Operação ApproximatelyApplyDiagonalUnitary
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApproximatelyApplyDiagonalUnitary
qsharp.summary: Applies an array of complex phases to numeric basis states of a register of qubits, truncating small rotation angles according to a given tolerance.
ms.openlocfilehash: 5d8f6646c124f4296b9cd2abd71e73de5a530e55
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850347"
---
# <a name="approximatelyapplydiagonalunitary-operation"></a>Operação ApproximatelyApplyDiagonalUnitary

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma matriz de fases complexas a Estados de base numéricos de um registro de qubits, truncando ângulos de rotação pequenos de acordo com uma determinada tolerância.

```qsharp
operation ApproximatelyApplyDiagonalUnitary (tolerance : Double, coefficients : Double[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Descrição

Esta operação implementa um unitário diagonal que aplica uma fase complexa $e ^ {i \ theta_j} $ no estado do número do $n $-qubit $ \ket{j} $.
Em particular, essa operação pode ser representada pelo unitário

$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} e ^ {i \ theta_j} \ket{j}\bra{j}.
\end{align} $ $

## <a name="input"></a>Entrada

### <a name="tolerance--double"></a>tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)

Uma tolerância abaixo que pequenos coeficientes são truncados.


### <a name="coefficients--double"></a>coeficientes: [duplo](xref:microsoft.quantum.lang-ref.double)[]

Matriz de até $2 ^ n $ coeficientes $ \ theta_j $. O coeficiente $j $ th indexa o estado de número $ \ket{j} $ codificado em um formato little-endian.


### <a name="qubits--littleendian"></a>qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n o registro de controle $-qubit que codifica Estados de número $ \ket{j} $ no formato little-endian.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

`coefficients` será preenchido com os elementos $ \ theta_j = $0 se menos de $2 ^ n $ forem especificados.

## <a name="references"></a>Referências

- Síntese de circuitos lógicos Quantum Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ApplyDiagonalUnitary](xref:Microsoft.Quantum.Canon.ApplyDiagonalUnitary)