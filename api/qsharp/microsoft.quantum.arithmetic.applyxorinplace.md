---
uid: Microsoft.Quantum.Arithmetic.ApplyXorInPlace
title: Operação ApplyXorInPlace
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyXorInPlace
qsharp.summary: Applies a bitwise-XOR operation between a classical integer and an integer represented by a register of qubits.
ms.openlocfilehash: b7fc20ac421d5cff9baa3fe05450c1564f123505
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210092"
---
# <a name="applyxorinplace-operation"></a>Operação ApplyXorInPlace

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma operação de XOR-bit entre um inteiro clássico e um inteiro representado por um registro de qubits.

```qsharp
operation ApplyXorInPlace (value : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Descrição

Aplica `X` operações a qubits em um registro little-endian com base em 1 bits em um inteiro.

Vamos indicar `value` por a e permitir que y seja um inteiro não assinado codificado em e, `target` em seguida, `InPlaceXorLE` executa uma operação fornecida pelo seguinte mapa: $ \ket{y}\rightarrow \ket{y\oplus a} $, em que $ \oplus $ é o operador OR exclusivo de bit a ponto.

## <a name="input"></a>Entrada

### <a name="value--int"></a>valor: [int](xref:microsoft.quantum.lang-ref.int)

Um inteiro que é considerado não negativo.


### <a name="target--littleendian"></a>destino: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Um registro Quantum que é usado para armazenar `value` em codificação little-endian.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

