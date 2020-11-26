---
uid: Microsoft.Quantum.Random.DrawRandomInt
title: Operação DrawRandomInt
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomInt
qsharp.summary: Draws a random integer in a given inclusive range.
ms.openlocfilehash: f7b6cb75f761e4c45295245ed4bd4fb82c592809
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192903"
---
# <a name="drawrandomint-operation"></a><span data-ttu-id="aa262-102">Operação DrawRandomInt</span><span class="sxs-lookup"><span data-stu-id="aa262-102">DrawRandomInt operation</span></span>

<span data-ttu-id="aa262-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="aa262-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="aa262-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="aa262-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="aa262-105">Desenha um inteiro aleatório em um determinado intervalo inclusivo.</span><span class="sxs-lookup"><span data-stu-id="aa262-105">Draws a random integer in a given inclusive range.</span></span>

```qsharp
operation DrawRandomInt (min : Int, max : Int) : Int
```


## <a name="input"></a><span data-ttu-id="aa262-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa262-106">Input</span></span>

### <a name="min--int"></a><span data-ttu-id="aa262-107">mín.: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="aa262-107">min : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="aa262-108">O menor inteiro a ser desenhado.</span><span class="sxs-lookup"><span data-stu-id="aa262-108">The smallest integer to be drawn.</span></span>


### <a name="max--int"></a><span data-ttu-id="aa262-109">máx.: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="aa262-109">max : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="aa262-110">O maior inteiro a ser desenhado.</span><span class="sxs-lookup"><span data-stu-id="aa262-110">The largest integer to be drawn.</span></span>



## <a name="output--int"></a><span data-ttu-id="aa262-111">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="aa262-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="aa262-112">Um número inteiro no intervalo inclusivo de `min` a `max` com probabilidade uniforme.</span><span class="sxs-lookup"><span data-stu-id="aa262-112">An integer in the inclusive range from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa262-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa262-113">Remarks</span></span>

<span data-ttu-id="aa262-114">Falha se `max <= min` .</span><span class="sxs-lookup"><span data-stu-id="aa262-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="aa262-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="aa262-115">See Also</span></span>

- [<span data-ttu-id="aa262-116">Microsoft. Quantum. DiscreteUniformDistribution</span><span class="sxs-lookup"><span data-stu-id="aa262-116">Microsoft.Quantum.DiscreteUniformDistribution</span></span>](xref:Microsoft.Quantum.DiscreteUniformDistribution)