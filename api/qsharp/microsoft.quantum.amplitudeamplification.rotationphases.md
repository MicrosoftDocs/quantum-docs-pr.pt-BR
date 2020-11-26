---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhases
title: Tipo definido pelo usuário RotationPhases
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhases
qsharp.summary: Phases for a sequence of single-qubit rotations in amplitude amplification.
ms.openlocfilehash: 60fcda7d58a19f8891e252ddb18b504afddf5514
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191356"
---
# <a name="rotationphases-user-defined-type"></a><span data-ttu-id="7bc79-102">Tipo definido pelo usuário RotationPhases</span><span class="sxs-lookup"><span data-stu-id="7bc79-102">RotationPhases user defined type</span></span>

<span data-ttu-id="7bc79-103">Namespace: [Microsoft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="7bc79-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="7bc79-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7bc79-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7bc79-105">Fases para uma sequência de rotações de qubit única na amplificação de amplitude.</span><span class="sxs-lookup"><span data-stu-id="7bc79-105">Phases for a sequence of single-qubit rotations in amplitude amplification.</span></span>

```qsharp

newtype RotationPhases = (Double[]);
```



## <a name="remarks"></a><span data-ttu-id="7bc79-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="7bc79-106">Remarks</span></span>

<span data-ttu-id="7bc79-107">O primeiro parâmetro é uma matriz de fases para reflexões, expressa como um produto de rotações de qubit único.</span><span class="sxs-lookup"><span data-stu-id="7bc79-107">The first parameter is an array of phases for reflections, expressed as a product of single-qubit rotations.</span></span>
<span data-ttu-id="7bc79-108">[ G.H.</span><span class="sxs-lookup"><span data-stu-id="7bc79-108">[ G.H.</span></span> <span data-ttu-id="7bc79-109">Baixa, I. L</span><span class="sxs-lookup"><span data-stu-id="7bc79-109">Low, I. L.</span></span> <span data-ttu-id="7bc79-110">Chuang, https://arxiv.org/abs/1707.05391 ].</span><span class="sxs-lookup"><span data-stu-id="7bc79-110">Chuang, https://arxiv.org/abs/1707.05391].</span></span>