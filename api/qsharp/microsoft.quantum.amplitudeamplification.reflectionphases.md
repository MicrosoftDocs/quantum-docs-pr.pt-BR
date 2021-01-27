---
uid: Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
title: Tipo definido pelo usuário ReflectionPhases
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ReflectionPhases
qsharp.summary: Phases for a sequence of partial reflections in amplitude amplification.
ms.openlocfilehash: fc3642b76c6e01f0709e78ea42c9ea7237389afa
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847173"
---
# <a name="reflectionphases-user-defined-type"></a><span data-ttu-id="6b6ec-102">Tipo definido pelo usuário ReflectionPhases</span><span class="sxs-lookup"><span data-stu-id="6b6ec-102">ReflectionPhases user defined type</span></span>

<span data-ttu-id="6b6ec-103">Namespace: [Microsoft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="6b6ec-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="6b6ec-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6b6ec-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6b6ec-105">Fases para uma sequência de reflexos parciais na amplificação de amplitude.</span><span class="sxs-lookup"><span data-stu-id="6b6ec-105">Phases for a sequence of partial reflections in amplitude amplification.</span></span>

```qsharp

newtype ReflectionPhases = (AboutStart : Double[], AboutTarget : Double[]);
```



## <a name="named-items"></a><span data-ttu-id="6b6ec-106">Itens nomeados</span><span class="sxs-lookup"><span data-stu-id="6b6ec-106">Named Items</span></span>

### <a name="aboutstart--double"></a><span data-ttu-id="6b6ec-107">AboutStart: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="6b6ec-107">AboutStart : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="6b6ec-108">Uma matriz de fases para reflexão sobre o estado de início.</span><span class="sxs-lookup"><span data-stu-id="6b6ec-108">An array of phases for reflection about the start state.</span></span>
### <a name="abouttarget--double"></a><span data-ttu-id="6b6ec-109">AboutTarget: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="6b6ec-109">AboutTarget : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="6b6ec-110">Uma matriz de fases para reflexão sobre o estado de destino.</span><span class="sxs-lookup"><span data-stu-id="6b6ec-110">An array of phases for reflection about the target state.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b6ec-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b6ec-111">Remarks</span></span>

<span data-ttu-id="6b6ec-112">Ambas as matrizes devem ter comprimento igual.</span><span class="sxs-lookup"><span data-stu-id="6b6ec-112">Both arrays must be of equal length.</span></span> <span data-ttu-id="6b6ec-113">Observe que em muitos casos, a primeira fase sobre o estado de início e a última fase sobre o estado de destino apresenta uma mudança de fase global e pode ser definida como $0 $.</span><span class="sxs-lookup"><span data-stu-id="6b6ec-113">Note that in many cases, the first phase about the start state and last phase about the target state introduces a global phase shift and may be set to $0$.</span></span>