---
uid: Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger
title: Operação IncrementPhaseByModularInteger
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementPhaseByModularInteger
qsharp.summary: Performs a modular increment of a qubit register by an integer constant.
ms.openlocfilehash: 52309c056a3eae25ffdfbfa848f94bf744c71132
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694774"
---
# <a name="incrementphasebymodularinteger-operation"></a>Operação IncrementPhaseByModularInteger

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Agrupa [](https://nuget.org/packages/)


Executa um incremento modular de um registro qubit por uma constante de inteiro.

```qsharp
operation IncrementPhaseByModularInteger (increment : Int, modulus : Int, target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit
```


## <a name="description"></a>Descrição

Vamos indicar `increment` por $a $, `modulus` por $N $ e inteiro codificado `target` por $y $.
Em seguida, a operação executa a seguinte transformação: \begin{align} \ket{y} \mapsto \ket{(y + a) \operatorname{mod} N} \end{align} inteiros são codificados no formato little-endian na base QFT.

## <a name="input"></a>Entrada

### <a name="increment--int"></a>incremento: [int](xref:microsoft.quantum.lang-ref.int)

Incremento inteiro $a $ a ser adicionado a $y $.


### <a name="modulus--int"></a>módulo: [int](xref:microsoft.quantum.lang-ref.int)

Integer $N $ que mods $y + a $.


### <a name="target--phaselittleendian"></a>destino: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)

Integer $y $ no formato little-endian codificado em fases que `increment` $a $ é adicionado a.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

Pressupõe que `target` tem o bit mais alto definido como 0.
Também pressupõe que o valor de destino seja menor que $N $.

Para o diagrama de circuito e a explicação, consulte a Figura 5 na [página 5 de arXiv: Quant-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=5).

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. aritmético. IncrementByModularInteger](xref:Microsoft.Quantum.Arithmetic.IncrementByModularInteger)