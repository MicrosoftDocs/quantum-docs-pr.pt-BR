---
uid: Microsoft.Quantum.Arithmetic.IncrementByModularInteger
title: Operação IncrementByModularInteger
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementByModularInteger
qsharp.summary: Performs a modular increment of a qubit register by an integer constant.
ms.openlocfilehash: 8a02d22facce8f58180752b6d063ac55d75ca537
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222942"
---
# <a name="incrementbymodularinteger-operation"></a>Operação IncrementByModularInteger

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Executa um incremento modular de um registro qubit por uma constante de inteiro.

```qsharp
operation IncrementByModularInteger (increment : Int, modulus : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Descrição

Vamos indicar `increment` por $a $, `modulus` por $N $ e inteiro codificado `target` por $y $.
Em seguida, a operação executa a seguinte transformação: \begin{align} \ket{y} \mapsto \ket{(y + a) \operatorname{mod} N} \end{align} inteiros são codificados no formato little-endian.

## <a name="input"></a>Entrada

### <a name="increment--int"></a>incremento: [int](xref:microsoft.quantum.lang-ref.int)

Incremento inteiro $a $ a ser adicionado a $y $.


### <a name="modulus--int"></a>módulo: [int](xref:microsoft.quantum.lang-ref.int)

Integer $N $ que mods $y + a $.


### <a name="target--littleendian"></a>destino: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Inteiro $y $ no `LittleEndian` formato `increment` ao qual $a $ é adicionado.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

Pressupõe que o valor inicial de destino seja menor que $N $ e que o incremento $a $ seja menor que $N $.
Observe que <xref:microsoft.quantum.arithmetic.incrementphasebymodularinteger> o implementa a mesma operação na `PhaseLittleEndian` base.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. aritmético. IncrementPhaseByModularInteger](xref:Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger)