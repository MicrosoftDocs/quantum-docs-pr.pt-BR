---
uid: Microsoft.Quantum.Simulation.BlockEncodingReflectionByLCU
title: Função BlockEncodingReflectionByLCU
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingReflectionByLCU
qsharp.summary: >-
  Encodes an operator of interest into a `BlockEncodingReflection`.

  This constructs a `BlockEncodingReflection` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries. Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.
ms.openlocfilehash: e1247d961a7ebce798106c24c46d924dd6e6d347
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229470"
---
# <a name="blockencodingreflectionbylcu-function"></a>Função BlockEncodingReflectionByLCU

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Codifica um operador de interesse em um `BlockEncodingReflection` .

Isso constrói um `BlockEncodingReflection` unitário $U = P\cdot V\cdot P ^ \dagger $ que codifica algum operador $H = \ sum_ {j} | \ alpha_j | U_j $ de interesse que é uma combinação linear de unidades. Normalmente, $P $ é uma \ket de preparação de estado, de modo que $P {0} \_ a \ sum_j \sqrt{\ alpha_j/ \| \vec\alpha \| \_ 2} \ket{j} \_ a $ e $V = \ sum_ {j} \ket{j}\bra{j} \_ a\otimes U_j $.

```qsharp
function BlockEncodingReflectionByLCU (statePreparation : (Qubit[] => Unit is Adj + Ctl), selector : ((Qubit[], Qubit[]) => Unit is Adj + Ctl)) : Microsoft.Quantum.Simulation.BlockEncodingReflection
```


## <a name="input"></a>Entrada

### <a name="statepreparation--qubit--unit--is-adj--ctl"></a>statePreparation: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL

Um unitário $P $ que prepara algum estado de destino.


### <a name="selector--qubitqubit--unit--is-adj--ctl"></a>seletor: ([qubit](xref:microsoft.quantum.lang-ref.qubit)[],[qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL

Um unitário $V $ que codifica as unidades de componente de $H $.



## <a name="output--blockencodingreflection"></a>Saída: [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)

Um unitário $U $ agindo em conjunto em registros `a` e `s` que os codificadores de bloco $H $ e satisfaz $U ' ^ {-1} = U $.

## <a name="remarks"></a>Comentários

Essa `BlockEncoding` implementação fornece as propriedades de um `BlockEncodingReflection` .

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Simulation. BlockEncoding](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [Microsoft. Quantum. Simulation. BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)