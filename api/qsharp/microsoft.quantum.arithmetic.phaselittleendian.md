---
uid: Microsoft.Quantum.Arithmetic.PhaseLittleEndian
title: Tipo definido pelo usuário PhaseLittleEndian
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: PhaseLittleEndian
qsharp.summary: >-
  Little-endian unsigned integers in QFT basis.

  For example, if $\ket{x}$ is the little-endian encoding of the integer $x$ in the computational basis, then $\operatorname{QFTLE} \ket{x}$ is the encoding of $x$ in the QFT basis.
ms.openlocfilehash: 45b824a74d664df0d5707264a3c616fb27c477b3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222415"
---
# <a name="phaselittleendian-user-defined-type"></a>Tipo definido pelo usuário PhaseLittleEndian

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Inteiros sem sinal de little endian na base QFT.

Por exemplo, se $ \ket{x} $ for a codificação little-endian do inteiro $x $ na base computacional, $ \operatorname{QFTLE} \ket{x} $ será a codificação de $x $ na base QFT.

```qsharp

newtype PhaseLittleEndian = (Qubit[]);
```



## <a name="remarks"></a>Comentários

Abreviamos `PhaseLittleEndian` como `PhaseLE` na documentação.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. QFT](xref:Microsoft.Quantum.Canon.QFT)
- [Microsoft. Quantum. Canon. QFTLE](xref:Microsoft.Quantum.Canon.QFTLE)