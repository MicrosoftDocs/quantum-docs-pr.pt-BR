---
uid: Microsoft.Quantum.Arithmetic.MultiplyByModularInteger
title: Operação MultiplyByModularInteger
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyByModularInteger
qsharp.summary: Performs modular multiplication by an integer constant on a qubit register.
ms.openlocfilehash: 080414d208a2a0c114857db8e93efb4cd74a4d8d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222568"
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