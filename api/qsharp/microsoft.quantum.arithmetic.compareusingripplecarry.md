---
uid: Microsoft.Quantum.Arithmetic.CompareUsingRippleCarry
title: Operação CompareUsingRippleCarry
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareUsingRippleCarry
qsharp.summary: This operation tests if an integer represented by a register of qubits is greater than another integer, applying an XOR of the result onto an output qubit.
ms.openlocfilehash: ce2be140ecfed21dea6212651249b4a11d2542c8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843283"
---
# <a name="compareusingripplecarry-operation"></a>Operação CompareUsingRippleCarry

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Esta operação testa se um inteiro representado por um registro de qubits é maior que outro inteiro, aplicando um XOR do resultado em um qubit de saída.

```qsharp
operation CompareUsingRippleCarry (x : Microsoft.Quantum.Arithmetic.LittleEndian, y : Microsoft.Quantum.Arithmetic.LittleEndian, output : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>Descrição

Considerando dois inteiros `x` e `y` armazenados em registros de qubit de tamanho igual, essa operação verifica se eles atendem `x > y` . Se for true, 1 será XORed em um qubit de saída. Caso contrário, 0 será XORed em um qubit de saída.
Em outras palavras, essa operação pode ser representada pelo unitário $ $ \begin{align} U\ket {x} \ ket {y} \ ket {z} = \ket{x}\ket{y}\ket{z\oplus (x>y)}.
\end{align} $ $

## <a name="input"></a>Entrada

### <a name="x--littleendian"></a>x: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Primeiro número a ser comparado armazenado no `LittleEndian` formato em um registro de qubit.


### <a name="y--littleendian"></a>y: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Segundo número a ser comparado armazenado no `LittleEndian` formato em um registro de qubit.


### <a name="output--qubit"></a>saída: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit que armazena o resultado da comparação $x>y $.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Referências

- Um novo circuito do Quantum-transporte de adição de Altova-conjunto Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton https://arxiv.org/abs/quant-ph/0410184