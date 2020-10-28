---
uid: Microsoft.Quantum.Arithmetic.PhaseLittleEndian
title: Tipo definido pelo usuário PhaseLittleEndian
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: PhaseLittleEndian
qsharp.summary: >-
  Little-endian unsigned integers in QFT basis.

  For example, if $\ket{x}$ is the little-endian encoding of the integer $x$ in the computational basis, then $\operatorname{QFTLE} \ket{x}$ is the encoding of $x$ in the QFT basis.
ms.openlocfilehash: f1f792d62004a2765d4e63870f5a41a4377b0d34
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694553"
---
# <a name="phaselittleendian-user-defined-type"></a>Tipo definido pelo usuário PhaseLittleEndian

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Agrupa [](https://nuget.org/packages/)


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