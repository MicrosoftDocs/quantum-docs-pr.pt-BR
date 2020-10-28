---
uid: Microsoft.Quantum.Random.ContinuousUniformDistribution
title: Função ContinuousUniformDistribution
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: ContinuousUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive interval.
ms.openlocfilehash: 74300efb10ba7b5aa006f0b1b6aafde0da840f00
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693045"
---
# <a name="continuousuniformdistribution-function"></a><span data-ttu-id="4206f-102">Função ContinuousUniformDistribution</span><span class="sxs-lookup"><span data-stu-id="4206f-102">ContinuousUniformDistribution function</span></span>

<span data-ttu-id="4206f-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="4206f-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="4206f-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4206f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4206f-105">Retorna uma distribuição uniforme em um determinado intervalo inclusivo.</span><span class="sxs-lookup"><span data-stu-id="4206f-105">Returns a uniform distribution over a given inclusive interval.</span></span>

```qsharp
function ContinuousUniformDistribution (min : Double, max : Double) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a><span data-ttu-id="4206f-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="4206f-106">Input</span></span>

### <a name="min--double"></a><span data-ttu-id="4206f-107">mín.: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="4206f-107">min : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="4206f-108">O menor número real a ser desenhado.</span><span class="sxs-lookup"><span data-stu-id="4206f-108">The smallest real number to be drawn.</span></span>


### <a name="max--double"></a><span data-ttu-id="4206f-109">máx.: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="4206f-109">max : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="4206f-110">O maior número real a ser desenhado.</span><span class="sxs-lookup"><span data-stu-id="4206f-110">The largest real number to be drawn.</span></span>



## <a name="output--continuousdistribution"></a><span data-ttu-id="4206f-111">Saída: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="4206f-111">Output : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="4206f-112">Uma distribuição cujos variates aleatórios são números reais no intervalo inclusivo de `min` a `max` com probabilidade uniforme.</span><span class="sxs-lookup"><span data-stu-id="4206f-112">A distribution whose random variates are real numbers in the inclusive interval from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="4206f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4206f-113">Remarks</span></span>

<span data-ttu-id="4206f-114">Falha se `max <= min` .</span><span class="sxs-lookup"><span data-stu-id="4206f-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="4206f-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="4206f-115">See Also</span></span>

- [<span data-ttu-id="4206f-116">Microsoft. Quantum. DrawRandomDouble</span><span class="sxs-lookup"><span data-stu-id="4206f-116">Microsoft.Quantum.DrawRandomDouble</span></span>](xref:Microsoft.Quantum.DrawRandomDouble)