---
uid: Microsoft.Quantum.Arithmetic.PhaseLittleEndian
title: Tipo definido pelo usuário PhaseLittleEndian
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: PhaseLittleEndian
qsharp.summary: >-
  Little-endian unsigned integers in QFT basis.

  For example, if $\ket{x}$ is the little-endian encoding of the integer $x$ in the computational basis, then $\operatorname{QFTLE} \ket{x}$ is the encoding of $x$ in the QFT basis.
ms.openlocfilehash: 59df1db31090f875ccd261fe6cc43995ba57b963
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842993"
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