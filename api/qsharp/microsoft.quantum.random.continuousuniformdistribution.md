---
uid: Microsoft.Quantum.Random.ContinuousUniformDistribution
title: Função ContinuousUniformDistribution
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: ContinuousUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive interval.
ms.openlocfilehash: a3911fe9962ce18daa239de0272c53d83344134a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193073"
---
# <a name="continuousuniformdistribution-function"></a><span data-ttu-id="fb59c-102">Função ContinuousUniformDistribution</span><span class="sxs-lookup"><span data-stu-id="fb59c-102">ContinuousUniformDistribution function</span></span>

<span data-ttu-id="fb59c-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="fb59c-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="fb59c-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="fb59c-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="fb59c-105">Retorna uma distribuição uniforme em um determinado intervalo inclusivo.</span><span class="sxs-lookup"><span data-stu-id="fb59c-105">Returns a uniform distribution over a given inclusive interval.</span></span>

```qsharp
function ContinuousUniformDistribution (min : Double, max : Double) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a><span data-ttu-id="fb59c-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="fb59c-106">Input</span></span>

### <a name="min--double"></a><span data-ttu-id="fb59c-107">mín.: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="fb59c-107">min : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="fb59c-108">O menor número real a ser desenhado.</span><span class="sxs-lookup"><span data-stu-id="fb59c-108">The smallest real number to be drawn.</span></span>


### <a name="max--double"></a><span data-ttu-id="fb59c-109">máx.: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="fb59c-109">max : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="fb59c-110">O maior número real a ser desenhado.</span><span class="sxs-lookup"><span data-stu-id="fb59c-110">The largest real number to be drawn.</span></span>



## <a name="output--continuousdistribution"></a><span data-ttu-id="fb59c-111">Saída: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="fb59c-111">Output : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="fb59c-112">Uma distribuição cujos variates aleatórios são números reais no intervalo inclusivo de `min` a `max` com probabilidade uniforme.</span><span class="sxs-lookup"><span data-stu-id="fb59c-112">A distribution whose random variates are real numbers in the inclusive interval from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb59c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb59c-113">Remarks</span></span>

<span data-ttu-id="fb59c-114">Falha se `max <= min` .</span><span class="sxs-lookup"><span data-stu-id="fb59c-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="fb59c-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="fb59c-115">See Also</span></span>

- [<span data-ttu-id="fb59c-116">Microsoft. Quantum. DrawRandomDouble</span><span class="sxs-lookup"><span data-stu-id="fb59c-116">Microsoft.Quantum.DrawRandomDouble</span></span>](xref:Microsoft.Quantum.DrawRandomDouble)