---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhases
title: Tipo definido pelo usuário RotationPhases
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhases
qsharp.summary: Phases for a sequence of single-qubit rotations in amplitude amplification.
ms.openlocfilehash: b0373f964b77f8ea561c6e96b11e476b42e7fc55
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694891"
---
# <a name="rotationphases-user-defined-type"></a><span data-ttu-id="b0640-102">Tipo definido pelo usuário RotationPhases</span><span class="sxs-lookup"><span data-stu-id="b0640-102">RotationPhases user defined type</span></span>

<span data-ttu-id="b0640-103">Namespace: [Microsoft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="b0640-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="b0640-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b0640-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b0640-105">Fases para uma sequência de rotações de qubit única na amplificação de amplitude.</span><span class="sxs-lookup"><span data-stu-id="b0640-105">Phases for a sequence of single-qubit rotations in amplitude amplification.</span></span>

```qsharp

newtype RotationPhases = (Double[]);
```



## <a name="remarks"></a><span data-ttu-id="b0640-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0640-106">Remarks</span></span>

<span data-ttu-id="b0640-107">O primeiro parâmetro é uma matriz de fases para reflexões, expressa como um produto de rotações de qubit único.</span><span class="sxs-lookup"><span data-stu-id="b0640-107">The first parameter is an array of phases for reflections, expressed as a product of single-qubit rotations.</span></span>
<span data-ttu-id="b0640-108">[ G.H.</span><span class="sxs-lookup"><span data-stu-id="b0640-108">[ G.H.</span></span> <span data-ttu-id="b0640-109">Baixa, I. L</span><span class="sxs-lookup"><span data-stu-id="b0640-109">Low, I. L.</span></span> <span data-ttu-id="b0640-110">Chuang, https://arxiv.org/abs/1707.05391 ].</span><span class="sxs-lookup"><span data-stu-id="b0640-110">Chuang, https://arxiv.org/abs/1707.05391].</span></span>