---
uid: Microsoft.Quantum.Arithmetic.CompareGTSI
title: Operação CompareGTSI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGTSI
qsharp.summary: 'Wrapper for signed integer comparison: `result = xs > ys`.'
ms.openlocfilehash: f725bdbaa945a4f87e90fc71930c37642113c21a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846702"
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

