---
uid: Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger
title: Operação MultiplyAndAddByModularInteger
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyAndAddByModularInteger
qsharp.summary: Performs a modular multiply-and-add by integer constants on a qubit register.
ms.openlocfilehash: e4de934a5776e80dbf5f0d8334bf806e6a84b743
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846508"
---
# <a name="multiplyandaddbymodularinteger-operation"></a>Operação MultiplyAndAddByModularInteger

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Executa uma multiplicação modular e adicionar por constantes de inteiro em um registro de qubit.

```qsharp
operation MultiplyAndAddByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian, summand : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Descrição

Implementa o MAP $ $ \begin{align} \ket{x} \ket{b} \mapsto \ket{x} \ket{(b + a \cdot x) \operatorname{mod} N} \end{align} $ $ para um determinado módulo $N $, um multiplicador constante $a $ e soma $y $.

## <a name="input"></a>Entrada

### <a name="constmultiplier--int"></a>constMultiplier: [int](xref:microsoft.quantum.lang-ref.int)

Um inteiro $a $ a ser adicionado a cada rótulo de estado base.


### <a name="modulus--int"></a>módulo: [int](xref:microsoft.quantum.lang-ref.int)

O módulo $N $ que adição e multiplicação são tomadas em relação a.


### <a name="multiplier--littleendian"></a>multiplicador: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Um registro Quantum que representa um inteiro sem sinal cujo valor deve ser adicionado a cada rótulo de estado base de `summand` .


### <a name="summand--littleendian"></a>soma: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Um registro Quantum que representa um inteiro não assinado para usar como o destino para esta operação.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

- Para o diagrama de circuito e a explicação, consulte a Figura 6 na [página 7 de arXiv: Quant-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=7)
- Esta operação corresponde a CMULT (a) MOD (N) em [arXiv: Quant-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf)

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. aritmético. MultiplyAndAddPhaseByModularInteger](xref:Microsoft.Quantum.Arithmetic.MultiplyAndAddPhaseByModularInteger)