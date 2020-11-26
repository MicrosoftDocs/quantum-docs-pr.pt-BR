---
uid: Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE
title: Operação ApplyQuantumFourierTransformBE
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyQuantumFourierTransformBE
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.
ms.openlocfilehash: 39db7b4c69f7f06418ec257c013837c65b9cc67a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209036"
---
# <a name="applyquantumfouriertransformbe-operation"></a>Operação ApplyQuantumFourierTransformBE

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Executa a transformação de Fourier do Quantum em um registro do Quantum contendo um número inteiro na representação big-endian.

```qsharp
operation ApplyQuantumFourierTransformBE (qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="qs--bigendian"></a>QS: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)

Quantum registrado para o qual a transformação de Fourier do Quantum é aplicada



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

Presume-se que a entrada e a saída estejam em big endian codificação.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ApproximateQFT](xref:Microsoft.Quantum.Canon.ApproximateQFT)
- [Microsoft. Quantum. Canon. QFTLE](xref:Microsoft.Quantum.Canon.QFTLE)