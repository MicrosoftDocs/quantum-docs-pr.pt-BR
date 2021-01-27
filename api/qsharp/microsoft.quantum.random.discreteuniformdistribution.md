---
uid: Microsoft.Quantum.Random.DiscreteUniformDistribution
title: Função DiscreteUniformDistribution
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DiscreteUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive range.
ms.openlocfilehash: f909e7def5439ec0feef4ca4dc0cf8ed12374dfe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853714"
---
# <a name="discreteuniformdistribution-function"></a><span data-ttu-id="9f80b-102">Função DiscreteUniformDistribution</span><span class="sxs-lookup"><span data-stu-id="9f80b-102">DiscreteUniformDistribution function</span></span>

<span data-ttu-id="9f80b-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="9f80b-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="9f80b-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="9f80b-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="9f80b-105">Retorna uma distribuição uniforme em um determinado intervalo inclusivo.</span><span class="sxs-lookup"><span data-stu-id="9f80b-105">Returns a uniform distribution over a given inclusive range.</span></span>

```qsharp
function DiscreteUniformDistribution (min : Int, max : Int) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a><span data-ttu-id="9f80b-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="9f80b-106">Input</span></span>

### <a name="min--int"></a><span data-ttu-id="9f80b-107">mín.: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9f80b-107">min : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9f80b-108">O menor inteiro a ser desenhado.</span><span class="sxs-lookup"><span data-stu-id="9f80b-108">The smallest integer to be drawn.</span></span>


### <a name="max--int"></a><span data-ttu-id="9f80b-109">máx.: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9f80b-109">max : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9f80b-110">O maior inteiro a ser desenhado.</span><span class="sxs-lookup"><span data-stu-id="9f80b-110">The largest integer to be drawn.</span></span>



## <a name="output--discretedistribution"></a><span data-ttu-id="9f80b-111">Saída: [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="9f80b-111">Output : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="9f80b-112">Uma distribuição cujos variates aleatórios são inteiros no intervalo inclusivo de `min` a `max` com probabilidade uniforme.</span><span class="sxs-lookup"><span data-stu-id="9f80b-112">A distribution whose random variates are integers in the inclusive range from `min` to `max` with uniform probability.</span></span>

## <a name="example"></a><span data-ttu-id="9f80b-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="9f80b-113">Example</span></span>

<span data-ttu-id="9f80b-114">O trecho de código Q # a seguir acumula aleatoriamente uma matriz de seis lados:</span><span class="sxs-lookup"><span data-stu-id="9f80b-114">The following Q# snippet randomly rolls a six-sided die:</span></span>

```qsharp
let dieDistribution = DiscreteUniformDistribution(1, 6);
let dieRoll = dieDistribution::Sample();
```

## <a name="remarks"></a><span data-ttu-id="9f80b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f80b-115">Remarks</span></span>

<span data-ttu-id="9f80b-116">Falha se `max <= min` .</span><span class="sxs-lookup"><span data-stu-id="9f80b-116">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="9f80b-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="9f80b-117">See Also</span></span>

- [<span data-ttu-id="9f80b-118">Microsoft. Quantum. DrawRandomDouble</span><span class="sxs-lookup"><span data-stu-id="9f80b-118">Microsoft.Quantum.DrawRandomDouble</span></span>](xref:Microsoft.Quantum.DrawRandomDouble)