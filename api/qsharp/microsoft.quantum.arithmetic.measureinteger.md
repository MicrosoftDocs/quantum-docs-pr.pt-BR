---
uid: Microsoft.Quantum.Arithmetic.MeasureInteger
title: Operação MeasureInteger
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MeasureInteger
qsharp.summary: Measures the content of a quantum register and converts it to an integer. The measurement is performed with respect to the standard computational basis, i.e., the eigenbasis of `PauliZ`.
ms.openlocfilehash: e3ff06e5cbb2ef8a63e4ad12308b382347c90fc3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222636"
---
# <a name="measureinteger-operation"></a>Operação MeasureInteger

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Mede o conteúdo de um Quantum registrado e o converte em um inteiro. A medida é executada em relação à base computacional padrão, ou seja, a eigenbasis de `PauliZ` .

```qsharp
operation MeasureInteger (target : Microsoft.Quantum.Arithmetic.LittleEndian) : Int
```


## <a name="input"></a>Entrada

### <a name="target--littleendian"></a>destino: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Um registro da Quantum na codificação little-endian.



## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)

Um inteiro sem sinal que contém o valor medido de `target` .

## <a name="remarks"></a>Comentários

Esta operação redefine seu registro de entrada para o estado $ \ket{00\cdots 0} $, adequado para a liberação de volta para um computador de destino.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. MeasureIntegerBE](xref:Microsoft.Quantum.Canon.MeasureIntegerBE)