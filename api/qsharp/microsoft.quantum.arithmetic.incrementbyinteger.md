---
uid: Microsoft.Quantum.Arithmetic.IncrementByInteger
title: Operação IncrementByInteger
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementByInteger
qsharp.summary: Increments an unsigned quantum register by a classical integer, using phase rotations.
ms.openlocfilehash: fa5e75e91206aa5f33233c8a54d6e9e7ac2950e3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222959"
---
# <a name="incrementbyinteger-operation"></a>Operação IncrementByInteger

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Incrementa um registro de Quantum não assinado por um inteiro clássico, usando rotações de fase.

```qsharp
operation IncrementByInteger (increment : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Descrição

Suponha que `target` o codifica um inteiro sem sinal $x $ em uma codificação little-endian e que `increment` seja igual a $a $.
Em seguida, essa operação implementa o unitário $ \ket{x} \mapsto \ket{x + a} $, em que a adição é executada módulo $2 ^ n $, em que $n = \texttt{Length (Target!)} $.

## <a name="input"></a>Entrada

### <a name="increment--int"></a>incremento: [int](xref:microsoft.quantum.lang-ref.int)

O inteiro pelo qual o `target` é incrementado por.


### <a name="target--littleendian"></a>destino: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Uma Quantum registra a codificação de um inteiro não assinado usando a codificação little-endian.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

