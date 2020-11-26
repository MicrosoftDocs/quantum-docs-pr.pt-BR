---
uid: Microsoft.Quantum.Arithmetic.MultiplyAndAddPhaseByModularInteger
title: Operação MultiplyAndAddPhaseByModularInteger
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyAndAddPhaseByModularInteger
qsharp.summary: The same as MultiplyAndAddByModularInteger, but assumes that the summand encodes integers in QFT basis.
ms.openlocfilehash: 1ca20b525d2a76e554d5a2e8d4f40060b5ef51cf
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223860"
---
# <a name="multiplyandaddphasebymodularinteger-operation"></a>Operação MultiplyAndAddPhaseByModularInteger

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


O mesmo que MultiplyAndAddByModularInteger, mas pressupõe que o soma codifica inteiros na base de QFT.

```qsharp
operation MultiplyAndAddPhaseByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian, phaseSummand : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="constmultiplier--int"></a>constMultiplier: [int](xref:microsoft.quantum.lang-ref.int)

Um inteiro $a $ a ser adicionado a cada rótulo de estado base.


### <a name="modulus--int"></a>módulo: [int](xref:microsoft.quantum.lang-ref.int)

O módulo $N $ que adição e multiplicação são tomadas em relação a.


### <a name="multiplier--littleendian"></a>multiplicador: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Um registro Quantum que representa um inteiro sem sinal cujo valor deve ser adicionado a cada rótulo de estado base de `summand` .


### <a name="phasesummand--phaselittleendian"></a>phaseSummand: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)

Um registro Quantum que representa um inteiro não assinado para usar como o destino para esta operação.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

Pressupõe que `phaseSummand` tem o bit mais alto definido como 0.
Também pressupõe que o valor de `phaseSummand` é menor que $N $.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. aritmético. MultiplyAndAddByModularInteger](xref:Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger)