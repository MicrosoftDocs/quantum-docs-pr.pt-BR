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
# <a name="phaselittleendian-user-defined-type"></a><span data-ttu-id="a0f8f-102">Tipo definido pelo usuário PhaseLittleEndian</span><span class="sxs-lookup"><span data-stu-id="a0f8f-102">PhaseLittleEndian user defined type</span></span>

<span data-ttu-id="a0f8f-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="a0f8f-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="a0f8f-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a0f8f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a0f8f-105">Inteiros sem sinal de little endian na base QFT.</span><span class="sxs-lookup"><span data-stu-id="a0f8f-105">Little-endian unsigned integers in QFT basis.</span></span>

<span data-ttu-id="a0f8f-106">Por exemplo, se $ \ket{x} $ for a codificação little-endian do inteiro $x $ na base computacional, $ \operatorname{QFTLE} \ket{x} $ será a codificação de $x $ na base QFT.</span><span class="sxs-lookup"><span data-stu-id="a0f8f-106">For example, if $\ket{x}$ is the little-endian encoding of the integer $x$ in the computational basis, then $\operatorname{QFTLE} \ket{x}$ is the encoding of $x$ in the QFT basis.</span></span>

```qsharp

newtype PhaseLittleEndian = (Qubit[]);
```



## <a name="remarks"></a><span data-ttu-id="a0f8f-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0f8f-107">Remarks</span></span>

<span data-ttu-id="a0f8f-108">Abreviamos `PhaseLittleEndian` como `PhaseLE` na documentação.</span><span class="sxs-lookup"><span data-stu-id="a0f8f-108">We abbreviate `PhaseLittleEndian` as `PhaseLE` in the documentation.</span></span>

## <a name="see-also"></a><span data-ttu-id="a0f8f-109">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="a0f8f-109">See Also</span></span>

- [<span data-ttu-id="a0f8f-110">Microsoft. Quantum. Canon. QFT</span><span class="sxs-lookup"><span data-stu-id="a0f8f-110">Microsoft.Quantum.Canon.QFT</span></span>](xref:Microsoft.Quantum.Canon.QFT)
- [<span data-ttu-id="a0f8f-111">Microsoft. Quantum. Canon. QFTLE</span><span class="sxs-lookup"><span data-stu-id="a0f8f-111">Microsoft.Quantum.Canon.QFTLE</span></span>](xref:Microsoft.Quantum.Canon.QFTLE)