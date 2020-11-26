---
uid: Microsoft.Quantum.Arithmetic.ComputeReciprocalI
title: Operação ComputeReciprocalI
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ComputeReciprocalI
qsharp.summary: Computes the reciprocal 1/x for an unsigned integer x using integer division. The result, interpreted as an integer, will be `floor(2^(2*n-1) / x)`.
ms.openlocfilehash: 9024da4a457265c65a41ef681cfbb99ebd4989a5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223350"
---
# <a name="computereciprocali-operation"></a>Operação ComputeReciprocalI

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Computa o 1/x recíproco para um inteiro sem sinal x usando divisão de inteiro. O resultado, interpretado como um inteiro, será `floor(2^(2*n-1) / x)` .

```qsharp
operation ComputeReciprocalI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="xs--littleendian"></a>xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

inteiro sem sinal de n bits


### <a name="result--littleendian"></a>resultado: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

2n-bit output, deve estar em $ \ket {0} $ inicialmente.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

Para a entrada x = 0, a saída será All-The.