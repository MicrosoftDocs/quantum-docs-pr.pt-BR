---
uid: Microsoft.Quantum.Arithmetic.MultiplyByModularInteger
title: Operação MultiplyByModularInteger
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyByModularInteger
qsharp.summary: Performs modular multiplication by an integer constant on a qubit register.
ms.openlocfilehash: bd4e0ad6c5bad779d9a31139690021fd9fcda210
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846504"
---
# <a name="multiplybymodularinteger-operation"></a>Operação MultiplyByModularInteger

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Executa a multiplicação modular por uma constante de inteiro em um registro de qubit.

```qsharp
operation MultiplyByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Descrição

Vamos indicar `modulus` por $N $ e `constMultiplier` $a $.
Em seguida, essa operação implementa uma operação unitário definida pelo seguinte mapa na base computacional: $ $ \begin{align} \ket{y} \mapsto \ket{(\cdot y) \operatorname{mod} N} \end{align} $ $ para todos os $y $ entre $0 $ e $N-$1.

## <a name="input"></a>Entrada

### <a name="constmultiplier--int"></a>constMultiplier: [int](xref:microsoft.quantum.lang-ref.int)

Constante pela qual multiplicador está sendo multiplicado. Deve ser coprimo para o módulo.


### <a name="modulus--int"></a>módulo: [int](xref:microsoft.quantum.lang-ref.int)

A operação de multiplicação é executada no módulo `modulus` .


### <a name="multiplier--littleendian"></a>multiplicador: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

O número que está sendo multiplicado por uma constante.
Esta é uma matriz de codificação qubits de um inteiro no formato little-endian.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

- Para o diagrama de circuito e a explicação, consulte a Figura 7 na [página 8 de arXiv: Quant-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=8)
- Esta operação corresponde a U ₐ em [arXiv: Quant-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf)