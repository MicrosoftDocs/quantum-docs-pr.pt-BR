---
uid: Microsoft.Quantum.Arithmetic.CompareGTI
title: Operação CompareGTI
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGTI
qsharp.summary: 'Wrapper for integer comparison: `result = x > y`.'
ms.openlocfilehash: b6e82eb7e9c068eff5bb320bb797a8fb0f8f921b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223469"
---
# <a name="comparegti-operation"></a>Operação CompareGTI

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Wrapper para comparação de números inteiros: `result = x > y` .

```qsharp
operation CompareGTI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="xs--littleendian"></a>xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Primeiro $n número de $-bit


### <a name="ys--littleendian"></a>haves: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Segundo $n número de $-bit


### <a name="result--qubit"></a>resultado: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Será invertido se $x > y $



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

