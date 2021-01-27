---
uid: Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger
title: Operação IncrementPhaseByModularInteger
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementPhaseByModularInteger
qsharp.summary: Performs a modular increment of a qubit register by an integer constant.
ms.openlocfilehash: 4ba35010d56ad01c73cb563646dc8150842da12e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846588"
---
# <a name="incrementphasebymodularinteger-operation"></a>Operação IncrementPhaseByModularInteger

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Executa um incremento modular de um registro qubit por uma constante de inteiro.

```qsharp
operation IncrementPhaseByModularInteger (increment : Int, modulus : Int, target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Adj + Ctl
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