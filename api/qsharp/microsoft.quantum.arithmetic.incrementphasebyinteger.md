---
uid: Microsoft.Quantum.Arithmetic.IncrementPhaseByInteger
title: Operação IncrementPhaseByInteger
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementPhaseByInteger
qsharp.summary: Increments an unsigned quantum register by a classical integer, using phase rotations.
ms.openlocfilehash: cc7922b2940cb979394958d5eb4e9933144eb062
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843156"
---
# <a name="incrementphasebyinteger-operation"></a>Operação IncrementPhaseByInteger

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Incrementa um registro de Quantum não assinado por um inteiro clássico, usando rotações de fase.

```qsharp
operation IncrementPhaseByInteger (increment : Int, target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Descrição

Suponha que `target` o codifica um inteiro sem sinal $x $ em uma codificação little-endian e que `increment` seja igual a $a $.
Em seguida, essa operação implementa o unitário $ \ket{x} \mapsto \ket{x + a} $, em que a adição é executada módulo $2 ^ n $, em que $n = \texttt{Length (Target!)} $.

## <a name="input"></a>Entrada

### <a name="increment--int"></a>incremento: [int](xref:microsoft.quantum.lang-ref.int)

O inteiro pelo qual o `target` é incrementado por.


### <a name="target--phaselittleendian"></a>destino: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)

Um Quantum registra a codificação de um inteiro não assinado usando a codificação little-endian na base dupla (QFT).



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

Observe que simplificamos o circuito porque o incremento é uma constante clássica, não um registro do Quantum.

Veja a figura na [ página 6 de arXiv: Quant-pH/0008033v1 ](https://arxiv.org/pdf/quant-ph/0008033.pdf#page=6) para o diagrama e a explicação do circuito.

## <a name="references"></a>Referências

- [*Thomas G. Draper*, arXiv: Quant-pH/0008033](https://arxiv.org/pdf/quant-ph/0008033v1.pdf)

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. aritmético. IncrementByInteger](xref:Microsoft.Quantum.Arithmetic.IncrementByInteger)