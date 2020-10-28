---
uid: Microsoft.Quantum.Arithmetic.IncrementByModularInteger
title: Operação IncrementByModularInteger
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementByModularInteger
qsharp.summary: Performs a modular increment of a qubit register by an integer constant.
ms.openlocfilehash: 271033b32b0de6cf600dca82126dab19c2bb4f5d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694781"
---
# <a name="incrementbymodularinteger-operation"></a>Operação IncrementByModularInteger

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Agrupa [](https://nuget.org/packages/)


Executa um incremento modular de um registro qubit por uma constante de inteiro.

```qsharp
operation IncrementByModularInteger (increment : Int, modulus : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
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