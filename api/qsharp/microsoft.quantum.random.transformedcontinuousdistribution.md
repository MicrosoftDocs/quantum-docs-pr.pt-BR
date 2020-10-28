---
uid: Microsoft.Quantum.Random.TransformedContinuousDistribution
title: Função TransformedContinuousDistribution
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: TransformedContinuousDistribution
qsharp.summary: Given a continuous distribution, returns a new distribution that transforms the original by a given function.
ms.openlocfilehash: 6a6e0c26bd650fd4c05208197ff23f951d1c3b5c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693261"
---
# <a name="transformedcontinuousdistribution-function"></a><span data-ttu-id="c6a40-102">Função TransformedContinuousDistribution</span><span class="sxs-lookup"><span data-stu-id="c6a40-102">TransformedContinuousDistribution function</span></span>

<span data-ttu-id="c6a40-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="c6a40-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="c6a40-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c6a40-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c6a40-105">Dada uma distribuição contínua, retorna uma nova distribuição que transforma o original por uma determinada função.</span><span class="sxs-lookup"><span data-stu-id="c6a40-105">Given a continuous distribution, returns a new distribution that transforms the original by a given function.</span></span>

```qsharp
function TransformedContinuousDistribution (transform : (Double -> Double), distribution : Microsoft.Quantum.Random.ContinuousDistribution) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a><span data-ttu-id="c6a40-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="c6a40-106">Input</span></span>

### <a name="transform--double---double"></a><span data-ttu-id="c6a40-107">transformação: [duplo](xref:microsoft.quantum.lang-ref.double) -> [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c6a40-107">transform : [Double](xref:microsoft.quantum.lang-ref.double) -> [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c6a40-108">Uma função que transforma variates da distribuição original para a distribuição transformada.</span><span class="sxs-lookup"><span data-stu-id="c6a40-108">A function that transforms variates of the original distribution to the transformed distribution.</span></span>


### <a name="distribution--continuousdistribution"></a><span data-ttu-id="c6a40-109">distribuição: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="c6a40-109">distribution : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="c6a40-110">A distribuição original a ser transformada.</span><span class="sxs-lookup"><span data-stu-id="c6a40-110">The original distribution to be transformed.</span></span>



## <a name="output--continuousdistribution"></a><span data-ttu-id="c6a40-111">Saída: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="c6a40-111">Output : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="c6a40-112">Uma nova distribuição relacionada à `distribution` transformação fornecida pelo `transform` .</span><span class="sxs-lookup"><span data-stu-id="c6a40-112">A new distribution related to `distribution` by the transformation given by `transform`.</span></span>