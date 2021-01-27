---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhasesAsReflectionPhases
title: Função RotationPhasesAsReflectionPhases
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhasesAsReflectionPhases
qsharp.summary: Converts phases specified as single-qubit rotations to phases specified as partial reflections.
ms.openlocfilehash: 5d50b3fdc2b0f948e93cb11b5c69403d97574ccd
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843949"
---
# <a name="rotationphasesasreflectionphases-function"></a><span data-ttu-id="e0fb6-102">Função RotationPhasesAsReflectionPhases</span><span class="sxs-lookup"><span data-stu-id="e0fb6-102">RotationPhasesAsReflectionPhases function</span></span>

<span data-ttu-id="e0fb6-103">Namespace: [Microsoft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="e0fb6-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="e0fb6-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e0fb6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e0fb6-105">Converte as fases especificadas como rotações de qubit único para fases especificadas como reflexos parciais.</span><span class="sxs-lookup"><span data-stu-id="e0fb6-105">Converts phases specified as single-qubit rotations to phases specified as partial reflections.</span></span>

```qsharp
function RotationPhasesAsReflectionPhases (rotPhases : Microsoft.Quantum.AmplitudeAmplification.RotationPhases) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a><span data-ttu-id="e0fb6-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="e0fb6-106">Input</span></span>

### <a name="rotphases--rotationphases"></a><span data-ttu-id="e0fb6-107">rotPhases: [RotationPhases](xref:Microsoft.Quantum.AmplitudeAmplification.RotationPhases)</span><span class="sxs-lookup"><span data-stu-id="e0fb6-107">rotPhases : [RotationPhases](xref:Microsoft.Quantum.AmplitudeAmplification.RotationPhases)</span></span>

<span data-ttu-id="e0fb6-108">Matriz de rotações de qubit único a serem convertidas em reflexões parciais.</span><span class="sxs-lookup"><span data-stu-id="e0fb6-108">Array of single-qubit rotations to be converted to partial reflections.</span></span>



## <a name="output--reflectionphases"></a><span data-ttu-id="e0fb6-109">Saída: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="e0fb6-109">Output : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="e0fb6-110">Uma operação que implementa as fases especificadas como reflexos parciais.</span><span class="sxs-lookup"><span data-stu-id="e0fb6-110">An operation that implements phases specified as partial reflections.</span></span>

## <a name="references"></a><span data-ttu-id="e0fb6-111">Referências</span><span class="sxs-lookup"><span data-stu-id="e0fb6-111">References</span></span>

<span data-ttu-id="e0fb6-112">Usamos a Convenção em</span><span class="sxs-lookup"><span data-stu-id="e0fb6-112">We use the convention in</span></span>

- <span data-ttu-id="e0fb6-113">[ *G.H. Low, I. L. Chuang*](https://arxiv.org/abs/1707.05391) para relacionar fases de rotação de qubit único a fases do operador de reflexão.</span><span class="sxs-lookup"><span data-stu-id="e0fb6-113">[ *G.H. Low, I. L. Chuang* ](https://arxiv.org/abs/1707.05391) for relating single-qubit rotation phases to reflection operator phases.</span></span>