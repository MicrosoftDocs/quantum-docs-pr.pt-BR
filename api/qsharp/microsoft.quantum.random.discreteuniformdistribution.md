---
uid: Microsoft.Quantum.Random.DiscreteUniformDistribution
title: Função DiscreteUniformDistribution
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DiscreteUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive range.
ms.openlocfilehash: 5e93c66d891d9b6aec548c0cf266df35e6090c92
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694647"
---
# <a name="discreteuniformdistribution-function"></a><span data-ttu-id="10214-102">Função DiscreteUniformDistribution</span><span class="sxs-lookup"><span data-stu-id="10214-102">DiscreteUniformDistribution function</span></span>

<span data-ttu-id="10214-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="10214-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="10214-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="10214-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="10214-105">Retorna uma distribuição uniforme em um determinado intervalo inclusivo.</span><span class="sxs-lookup"><span data-stu-id="10214-105">Returns a uniform distribution over a given inclusive range.</span></span>

```qsharp
function DiscreteUniformDistribution (min : Int, max : Int) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a><span data-ttu-id="10214-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="10214-106">Input</span></span>

### <a name="min--int"></a><span data-ttu-id="10214-107">mín.: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="10214-107">min : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="10214-108">O menor inteiro a ser desenhado.</span><span class="sxs-lookup"><span data-stu-id="10214-108">The smallest integer to be drawn.</span></span>


### <a name="max--int"></a><span data-ttu-id="10214-109">máx.: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="10214-109">max : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="10214-110">O maior inteiro a ser desenhado.</span><span class="sxs-lookup"><span data-stu-id="10214-110">The largest integer to be drawn.</span></span>



## <a name="output--discretedistribution"></a><span data-ttu-id="10214-111">Saída: [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="10214-111">Output : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="10214-112">Uma distribuição cujos variates aleatórios são inteiros no intervalo inclusivo de `min` a `max` com probabilidade uniforme.</span><span class="sxs-lookup"><span data-stu-id="10214-112">A distribution whose random variates are integers in the inclusive range from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="10214-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="10214-113">Remarks</span></span>

<span data-ttu-id="10214-114">Falha se `max <= min` .</span><span class="sxs-lookup"><span data-stu-id="10214-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="10214-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="10214-115">See Also</span></span>

- [<span data-ttu-id="10214-116">Microsoft. Quantum. DrawRandomDouble</span><span class="sxs-lookup"><span data-stu-id="10214-116">Microsoft.Quantum.DrawRandomDouble</span></span>](xref:Microsoft.Quantum.DrawRandomDouble)