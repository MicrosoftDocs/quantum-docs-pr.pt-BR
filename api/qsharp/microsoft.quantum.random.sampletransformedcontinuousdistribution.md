---
uid: Microsoft.Quantum.Random.SampleTransformedContinuousDistribution
title: Operação SampleTransformedContinuousDistribution
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: SampleTransformedContinuousDistribution
qsharp.summary: Internal-only operation for sampling from transformed distributions. Should only be used via partial application.
ms.openlocfilehash: dc93022e53199cd8ef794da9c1590d6997a0fda1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696876"
---
# <a name="sampletransformedcontinuousdistribution-operation"></a><span data-ttu-id="03a9c-102">Operação SampleTransformedContinuousDistribution</span><span class="sxs-lookup"><span data-stu-id="03a9c-102">SampleTransformedContinuousDistribution operation</span></span>

<span data-ttu-id="03a9c-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="03a9c-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="03a9c-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="03a9c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="03a9c-105">Operação somente interna para amostragem de distribuições transformadas.</span><span class="sxs-lookup"><span data-stu-id="03a9c-105">Internal-only operation for sampling from transformed distributions.</span></span>
<span data-ttu-id="03a9c-106">Só deve ser usado por meio de aplicativo parcial.</span><span class="sxs-lookup"><span data-stu-id="03a9c-106">Should only be used via partial application.</span></span>

```qsharp
operation SampleTransformedContinuousDistribution (transform : (Double -> Double), distribution : Microsoft.Quantum.Random.ContinuousDistribution) : Double
```


## <a name="input"></a><span data-ttu-id="03a9c-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="03a9c-107">Input</span></span>

### <a name="transform--double---double"></a><span data-ttu-id="03a9c-108">transformação: [duplo](xref:microsoft.quantum.lang-ref.double) -> [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="03a9c-108">transform : [Double](xref:microsoft.quantum.lang-ref.double) -> [Double](xref:microsoft.quantum.lang-ref.double)</span></span>




### <a name="distribution--continuousdistribution"></a><span data-ttu-id="03a9c-109">distribuição: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="03a9c-109">distribution : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>





## <a name="output--double"></a><span data-ttu-id="03a9c-110">Saída: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="03a9c-110">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

