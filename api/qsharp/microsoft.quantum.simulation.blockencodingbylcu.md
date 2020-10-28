---
uid: Microsoft.Quantum.Simulation.BlockEncodingByLCU
title: Função BlockEncodingByLCU
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingByLCU
qsharp.summary: >-
  Encodes an operator of interest into a `BlockEncoding`.

  This constructs a `BlockEncoding` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries. Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a=\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.
ms.openlocfilehash: 04738aa54ce8b719b05954824e3553388a995df0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92697003"
---
# <a name="blockencodingbylcu-function"></a>Função BlockEncodingByLCU

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Agrupa [](https://nuget.org/packages/)


Codifica um operador de interesse em um `BlockEncoding` .

Isso constrói um `BlockEncoding` unitário $U = P\cdot V\cdot P ^ \dagger $ que codifica algum operador $H = \ sum_ {j} | \ alpha_j | U_j $ de interesse que é uma combinação linear de unidades. Normalmente, $P $ é uma \ket de preparação de estado, de modo que $P {0} \_ a = \ sum_j \sqrt{\ alpha_j/ \| \vec\alpha \| \_ 2} \ket{j} \_ a $ e $V = \ sum_ {j} \ket{j}\bra{j} \_ a\otimes U_j $.

```qsharp
function BlockEncodingByLCU<'T, 'S> (statePreparation : ('T => Unit is Adj + Ctl), selector : (('T, 'S) => Unit is Adj + Ctl)) : (('T, 'S) => Unit is Adj + Ctl)
```


## <a name="input"></a>Entrada

### <a name="statepreparation--t--unit-adj--ctl"></a>statePreparation: t => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL

Um unitário $P $ que prepara algum estado de destino.


### <a name="selector--ts--unit-adj--ctl"></a>seletor: (t, ' s) => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL

Um unitário $V $ que codifica as unidades de componente de $H $.



## <a name="output--ts--unit-adj--ctl"></a>Saída: (t, ' s) => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL

Um unitário $U $ agindo em conjunto em registros `a` e `s` que os codificadores de bloco $H $ e satisfaz $U ^ \Dagger = U $.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'


### <a name="s"></a>Do



## <a name="remarks"></a>Comentários

Essa `BlockEncoding` implementação fornece as propriedades de um `BlockEncodingReflection` .

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Simulation. BlockEncoding](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [Microsoft. Quantum. Simulation. BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)