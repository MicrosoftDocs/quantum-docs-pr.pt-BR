---
uid: Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE
title: Operação ApplyQuantumFourierTransformBE
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyQuantumFourierTransformBE
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.
ms.openlocfilehash: a1f4a0a5e94465fc8bf3af344e2e19ee0d1d15e2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841575"
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