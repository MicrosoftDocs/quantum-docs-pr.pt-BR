---
uid: Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
title: Tipo definido pelo usuário ReflectionPhases
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ReflectionPhases
qsharp.summary: Phases for a sequence of partial reflections in amplitude amplification.
ms.openlocfilehash: e0c7db6cd1aad636a34684958be117de1b9888f8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694898"
---
# <a name="reflectionphases-user-defined-type"></a><span data-ttu-id="06a13-102">Tipo definido pelo usuário ReflectionPhases</span><span class="sxs-lookup"><span data-stu-id="06a13-102">ReflectionPhases user defined type</span></span>

<span data-ttu-id="06a13-103">Namespace: [Microsoft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="06a13-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="06a13-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="06a13-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="06a13-105">Fases para uma sequência de reflexos parciais na amplificação de amplitude.</span><span class="sxs-lookup"><span data-stu-id="06a13-105">Phases for a sequence of partial reflections in amplitude amplification.</span></span>

```qsharp

newtype ReflectionPhases = (AboutStart : Double[], AboutTarget : Double[]);
```



## <a name="named-items"></a><span data-ttu-id="06a13-106">Itens nomeados</span><span class="sxs-lookup"><span data-stu-id="06a13-106">Named Items</span></span>

### <a name="aboutstart--double"></a><span data-ttu-id="06a13-107">AboutStart: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="06a13-107">AboutStart : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="06a13-108">Uma matriz de fases para reflexão sobre o estado de início.</span><span class="sxs-lookup"><span data-stu-id="06a13-108">An array of phases for reflection about the start state.</span></span>
### <a name="abouttarget--double"></a><span data-ttu-id="06a13-109">AboutTarget: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="06a13-109">AboutTarget : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="06a13-110">Uma matriz de fases para reflexão sobre o estado de destino.</span><span class="sxs-lookup"><span data-stu-id="06a13-110">An array of phases for reflection about the target state.</span></span>

## <a name="remarks"></a><span data-ttu-id="06a13-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="06a13-111">Remarks</span></span>

<span data-ttu-id="06a13-112">Ambas as matrizes devem ter comprimento igual.</span><span class="sxs-lookup"><span data-stu-id="06a13-112">Both arrays must be of equal length.</span></span> <span data-ttu-id="06a13-113">Observe que em muitos casos, a primeira fase sobre o estado de início e a última fase sobre o estado de destino apresenta uma mudança de fase global e pode ser definida como $0 $.</span><span class="sxs-lookup"><span data-stu-id="06a13-113">Note that in many cases, the first phase about the start state and last phase about the target state introduces a global phase shift and may be set to $0$.</span></span>