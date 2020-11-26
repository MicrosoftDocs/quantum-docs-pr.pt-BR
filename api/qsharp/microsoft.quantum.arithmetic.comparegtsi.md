---
uid: Microsoft.Quantum.Arithmetic.CompareGTSI
title: Operação CompareGTSI
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGTSI
qsharp.summary: 'Wrapper for signed integer comparison: `result = xs > ys`.'
ms.openlocfilehash: a0e8ef66f1e1a62d4f6a78364135376810507534
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223486"
---
# <a name="comparegtsi-operation"></a>Operação CompareGTSI

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Wrapper para comparação de inteiros assinados: `result = xs > ys` .

```qsharp
operation CompareGTSI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, ys : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="xs--signedlittleendian"></a>xs: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)

Primeiro $n número de $-bit


### <a name="ys--signedlittleendian"></a>haves: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)

Segundo $n número de $-bit


### <a name="result--qubit"></a>resultado: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Será invertido se $xs > haves $



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

