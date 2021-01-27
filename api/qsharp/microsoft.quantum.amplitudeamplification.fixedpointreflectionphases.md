---
uid: Microsoft.Quantum.AmplitudeAmplification.FixedPointReflectionPhases
title: Função FixedPointReflectionPhases
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: FixedPointReflectionPhases
qsharp.summary: Computes partial reflection phases for fixed-point amplitude amplification.
ms.openlocfilehash: 2ded197801111c26d8a33f9c2363b46ca4b6c4b9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845852"
---
# <a name="fixedpointreflectionphases-function"></a><span data-ttu-id="0ec9c-102">Função FixedPointReflectionPhases</span><span class="sxs-lookup"><span data-stu-id="0ec9c-102">FixedPointReflectionPhases function</span></span>

<span data-ttu-id="0ec9c-103">Namespace: [Microsoft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="0ec9c-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="0ec9c-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0ec9c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0ec9c-105">Computa fases de reflexo parcial para amplificação de amplitude de ponto fixo.</span><span class="sxs-lookup"><span data-stu-id="0ec9c-105">Computes partial reflection phases for fixed-point amplitude amplification.</span></span>

```qsharp
function FixedPointReflectionPhases (nQueries : Int, successMin : Double) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a><span data-ttu-id="0ec9c-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="0ec9c-106">Input</span></span>

### <a name="nqueries--int"></a><span data-ttu-id="0ec9c-107">nQueries: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0ec9c-107">nQueries : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0ec9c-108">Número de consultas à preparação do estado Oracle.</span><span class="sxs-lookup"><span data-stu-id="0ec9c-108">Number of queries to the state preparation oracle.</span></span> <span data-ttu-id="0ec9c-109">Deve ser um inteiro ímpar.</span><span class="sxs-lookup"><span data-stu-id="0ec9c-109">Must be an odd integer.</span></span>


### <a name="successmin--double"></a><span data-ttu-id="0ec9c-110">successMin: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="0ec9c-110">successMin : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="0ec9c-111">Probabilidade de êxito mínima de destino.</span><span class="sxs-lookup"><span data-stu-id="0ec9c-111">Target minimum success probability.</span></span>



## <a name="output--reflectionphases"></a><span data-ttu-id="0ec9c-112">Saída: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="0ec9c-112">Output : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="0ec9c-113">Matriz de fases que pode ser usada na implementação do algoritmo Quantum da amplitude de ponto fixo.</span><span class="sxs-lookup"><span data-stu-id="0ec9c-113">Array of phases that can be used in fixed-point amplitude amplification quantum algorithm implementation.</span></span>

## <a name="references"></a><span data-ttu-id="0ec9c-114">Referências</span><span class="sxs-lookup"><span data-stu-id="0ec9c-114">References</span></span>

<span data-ttu-id="0ec9c-115">Usamos as fases em "amplificação de amplitude de ponto fixo com um número ideal de consultas"</span><span class="sxs-lookup"><span data-stu-id="0ec9c-115">We use the phases in "Fixed-Point Amplitude Amplification with an Optimal Number of Queries"</span></span>

- <span data-ttu-id="0ec9c-116">[YoderLowChuang2014](https://arxiv.org/abs/1409.3305) Consulte também "metodologia de Gates de Quantum de composição"</span><span class="sxs-lookup"><span data-stu-id="0ec9c-116">[YoderLowChuang2014](https://arxiv.org/abs/1409.3305) See also "Methodology of composite quantum gates"</span></span>
- <span data-ttu-id="0ec9c-117">[LowYoderChuang2016](https://arxiv.org/abs/1603.03996) para fases no `RotationPhases` formato.</span><span class="sxs-lookup"><span data-stu-id="0ec9c-117">[LowYoderChuang2016](https://arxiv.org/abs/1603.03996) for phases in the `RotationPhases` format.</span></span>