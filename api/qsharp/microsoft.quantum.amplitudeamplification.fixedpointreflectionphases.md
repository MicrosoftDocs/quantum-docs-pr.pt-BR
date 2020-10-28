---
uid: Microsoft.Quantum.AmplitudeAmplification.FixedPointReflectionPhases
title: Função FixedPointReflectionPhases
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: FixedPointReflectionPhases
qsharp.summary: Computes partial reflection phases for fixed-point amplitude amplification.
ms.openlocfilehash: 6ab2a8c6cb0b390f96aa13ece5d5b89c196a6107
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694904"
---
# <a name="fixedpointreflectionphases-function"></a><span data-ttu-id="b626f-102">Função FixedPointReflectionPhases</span><span class="sxs-lookup"><span data-stu-id="b626f-102">FixedPointReflectionPhases function</span></span>

<span data-ttu-id="b626f-103">Namespace: [Microsoft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="b626f-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="b626f-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b626f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b626f-105">Computa fases de reflexo parcial para amplificação de amplitude de ponto fixo.</span><span class="sxs-lookup"><span data-stu-id="b626f-105">Computes partial reflection phases for fixed-point amplitude amplification.</span></span>

```qsharp
function FixedPointReflectionPhases (nQueries : Int, successMin : Double) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a><span data-ttu-id="b626f-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="b626f-106">Input</span></span>

### <a name="nqueries--int"></a><span data-ttu-id="b626f-107">nQueries: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b626f-107">nQueries : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b626f-108">Número de consultas à preparação do estado Oracle.</span><span class="sxs-lookup"><span data-stu-id="b626f-108">Number of queries to the state preparation oracle.</span></span> <span data-ttu-id="b626f-109">Deve ser um inteiro ímpar.</span><span class="sxs-lookup"><span data-stu-id="b626f-109">Must be an odd integer.</span></span>


### <a name="successmin--double"></a><span data-ttu-id="b626f-110">successMin: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b626f-110">successMin : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b626f-111">Probabilidade de êxito mínima de destino.</span><span class="sxs-lookup"><span data-stu-id="b626f-111">Target minimum success probability.</span></span>



## <a name="output--reflectionphases"></a><span data-ttu-id="b626f-112">Saída: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="b626f-112">Output : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="b626f-113">Matriz de fases que pode ser usada na implementação do algoritmo Quantum da amplitude de ponto fixo.</span><span class="sxs-lookup"><span data-stu-id="b626f-113">Array of phases that can be used in fixed-point amplitude amplification quantum algorithm implementation.</span></span>

## <a name="references"></a><span data-ttu-id="b626f-114">Referências</span><span class="sxs-lookup"><span data-stu-id="b626f-114">References</span></span>

<span data-ttu-id="b626f-115">Usamos as fases em "amplificação de amplitude de ponto fixo com um número ideal de consultas"</span><span class="sxs-lookup"><span data-stu-id="b626f-115">We use the phases in "Fixed-Point Amplitude Amplification with an Optimal Number of Queries"</span></span>

- <span data-ttu-id="b626f-116">[YoderLowChuang2014](https://arxiv.org/abs/1409.3305) Consulte também "metodologia de Gates de Quantum de composição"</span><span class="sxs-lookup"><span data-stu-id="b626f-116">[YoderLowChuang2014](https://arxiv.org/abs/1409.3305) See also "Methodology of composite quantum gates"</span></span>
- <span data-ttu-id="b626f-117">[LowYoderChuang2016](https://arxiv.org/abs/1603.03996) para fases no `RotationPhases` formato.</span><span class="sxs-lookup"><span data-stu-id="b626f-117">[LowYoderChuang2016](https://arxiv.org/abs/1603.03996) for phases in the `RotationPhases` format.</span></span>