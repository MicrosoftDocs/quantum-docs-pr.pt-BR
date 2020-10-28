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
# <a name="phaselittleendian-user-defined-type"></a><span data-ttu-id="69ec5-102">Tipo definido pelo usuário PhaseLittleEndian</span><span class="sxs-lookup"><span data-stu-id="69ec5-102">PhaseLittleEndian user defined type</span></span>

<span data-ttu-id="69ec5-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="69ec5-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="69ec5-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="69ec5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="69ec5-105">Inteiros sem sinal de little endian na base QFT.</span><span class="sxs-lookup"><span data-stu-id="69ec5-105">Little-endian unsigned integers in QFT basis.</span></span>

<span data-ttu-id="69ec5-106">Por exemplo, se $ \ket{x} $ for a codificação little-endian do inteiro $x $ na base computacional, $ \operatorname{QFTLE} \ket{x} $ será a codificação de $x $ na base QFT.</span><span class="sxs-lookup"><span data-stu-id="69ec5-106">For example, if $\ket{x}$ is the little-endian encoding of the integer $x$ in the computational basis, then $\operatorname{QFTLE} \ket{x}$ is the encoding of $x$ in the QFT basis.</span></span>

```qsharp

newtype PhaseLittleEndian = (Qubit[]);
```



## <a name="remarks"></a><span data-ttu-id="69ec5-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="69ec5-107">Remarks</span></span>

<span data-ttu-id="69ec5-108">Abreviamos `PhaseLittleEndian` como `PhaseLE` na documentação.</span><span class="sxs-lookup"><span data-stu-id="69ec5-108">We abbreviate `PhaseLittleEndian` as `PhaseLE` in the documentation.</span></span>

## <a name="see-also"></a><span data-ttu-id="69ec5-109">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="69ec5-109">See Also</span></span>

- [<span data-ttu-id="69ec5-110">Microsoft. Quantum. Canon. QFT</span><span class="sxs-lookup"><span data-stu-id="69ec5-110">Microsoft.Quantum.Canon.QFT</span></span>](xref:Microsoft.Quantum.Canon.QFT)
- [<span data-ttu-id="69ec5-111">Microsoft. Quantum. Canon. QFTLE</span><span class="sxs-lookup"><span data-stu-id="69ec5-111">Microsoft.Quantum.Canon.QFTLE</span></span>](xref:Microsoft.Quantum.Canon.QFTLE)