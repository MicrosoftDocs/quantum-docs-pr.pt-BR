---
uid: Microsoft.Quantum.Random.DrawRandomInt
title: Operação DrawRandomInt
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomInt
qsharp.summary: Draws a random integer in a given inclusive range.
ms.openlocfilehash: d9d8d9fbb25587ac5ccbd4edf0e555649380375f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696974"
---
# <a name="drawrandomint-operation"></a><span data-ttu-id="54669-102">Operação DrawRandomInt</span><span class="sxs-lookup"><span data-stu-id="54669-102">DrawRandomInt operation</span></span>

<span data-ttu-id="54669-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="54669-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="54669-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="54669-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="54669-105">Desenha um inteiro aleatório em um determinado intervalo inclusivo.</span><span class="sxs-lookup"><span data-stu-id="54669-105">Draws a random integer in a given inclusive range.</span></span>

```qsharp
operation DrawRandomInt (min : Int, max : Int) : Int
```


## <a name="input"></a><span data-ttu-id="54669-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="54669-106">Input</span></span>

### <a name="min--int"></a><span data-ttu-id="54669-107">mín.: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="54669-107">min : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="54669-108">O menor inteiro a ser desenhado.</span><span class="sxs-lookup"><span data-stu-id="54669-108">The smallest integer to be drawn.</span></span>


### <a name="max--int"></a><span data-ttu-id="54669-109">máx.: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="54669-109">max : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="54669-110">O maior inteiro a ser desenhado.</span><span class="sxs-lookup"><span data-stu-id="54669-110">The largest integer to be drawn.</span></span>



## <a name="output--int"></a><span data-ttu-id="54669-111">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="54669-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="54669-112">Um número inteiro no intervalo inclusivo de `min` a `max` com probabilidade uniforme.</span><span class="sxs-lookup"><span data-stu-id="54669-112">An integer in the inclusive range from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="54669-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="54669-113">Remarks</span></span>

<span data-ttu-id="54669-114">Falha se `max <= min` .</span><span class="sxs-lookup"><span data-stu-id="54669-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="54669-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="54669-115">See Also</span></span>

- [<span data-ttu-id="54669-116">Microsoft. Quantum. DiscreteUniformDistribution</span><span class="sxs-lookup"><span data-stu-id="54669-116">Microsoft.Quantum.DiscreteUniformDistribution</span></span>](xref:Microsoft.Quantum.DiscreteUniformDistribution)