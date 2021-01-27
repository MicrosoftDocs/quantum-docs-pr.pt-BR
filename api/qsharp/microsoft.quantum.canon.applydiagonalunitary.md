---
uid: Microsoft.Quantum.Canon.ApplyDiagonalUnitary
title: Operação ApplyDiagonalUnitary
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyDiagonalUnitary
qsharp.summary: Applies an array of complex phases to numeric basis states of a register of qubits.
ms.openlocfilehash: 14ab8d7beddda26594967225934d472d52bac9eb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841898"
---
# <a name="applydiagonalunitary-operation"></a>Operação ApplyDiagonalUnitary

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma matriz de fases complexas a Estados de base numéricos de um registro de qubits.

```qsharp
operation ApplyDiagonalUnitary (coefficients : Double[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Descrição

Esta operação implementa um unitário diagonal que aplica uma fase complexa $e ^ {i \ theta_j} $ no estado do número do $n $-qubit $ \ket{j} $.
Em particular, essa operação pode ser representada pelo unitário

$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} e ^ {i \ theta_j} \ket{j}\bra{j}.
\end{align} $ $

## <a name="input"></a>Entrada

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

- [Microsoft. Quantum. Canon. ApproximatelyApplyDiagonalUnitary](xref:Microsoft.Quantum.Canon.ApproximatelyApplyDiagonalUnitary)