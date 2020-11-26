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
# <a name="phaselittleendian-user-defined-type"></a><span data-ttu-id="0561d-102">Tipo definido pelo usuário PhaseLittleEndian</span><span class="sxs-lookup"><span data-stu-id="0561d-102">PhaseLittleEndian user defined type</span></span>

<span data-ttu-id="0561d-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="0561d-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="0561d-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0561d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0561d-105">Inteiros sem sinal de little endian na base QFT.</span><span class="sxs-lookup"><span data-stu-id="0561d-105">Little-endian unsigned integers in QFT basis.</span></span>

<span data-ttu-id="0561d-106">Por exemplo, se $ \ket{x} $ for a codificação little-endian do inteiro $x $ na base computacional, $ \operatorname{QFTLE} \ket{x} $ será a codificação de $x $ na base QFT.</span><span class="sxs-lookup"><span data-stu-id="0561d-106">For example, if $\ket{x}$ is the little-endian encoding of the integer $x$ in the computational basis, then $\operatorname{QFTLE} \ket{x}$ is the encoding of $x$ in the QFT basis.</span></span>

```qsharp

newtype PhaseLittleEndian = (Qubit[]);
```



## <a name="remarks"></a><span data-ttu-id="0561d-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="0561d-107">Remarks</span></span>

<span data-ttu-id="0561d-108">Abreviamos `PhaseLittleEndian` como `PhaseLE` na documentação.</span><span class="sxs-lookup"><span data-stu-id="0561d-108">We abbreviate `PhaseLittleEndian` as `PhaseLE` in the documentation.</span></span>

## <a name="see-also"></a><span data-ttu-id="0561d-109">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="0561d-109">See Also</span></span>

- [<span data-ttu-id="0561d-110">Microsoft. Quantum. Canon. QFT</span><span class="sxs-lookup"><span data-stu-id="0561d-110">Microsoft.Quantum.Canon.QFT</span></span>](xref:Microsoft.Quantum.Canon.QFT)
- [<span data-ttu-id="0561d-111">Microsoft. Quantum. Canon. QFTLE</span><span class="sxs-lookup"><span data-stu-id="0561d-111">Microsoft.Quantum.Canon.QFTLE</span></span>](xref:Microsoft.Quantum.Canon.QFTLE)