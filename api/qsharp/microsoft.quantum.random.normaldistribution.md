---
uid: Microsoft.Quantum.Random.NormalDistribution
title: Função NormalDistribution
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: NormalDistribution
qsharp.summary: Returns a normal distribution with a given mean and variance.
ms.openlocfilehash: 733a2763dca6d75f81d538f63c3084331a8e1d51
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98814179"
---
# <a name="normaldistribution-function"></a><span data-ttu-id="5e0eb-102">Função NormalDistribution</span><span class="sxs-lookup"><span data-stu-id="5e0eb-102">NormalDistribution function</span></span>

<span data-ttu-id="5e0eb-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="5e0eb-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="5e0eb-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="5e0eb-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="5e0eb-105">Retorna uma distribuição normal com uma determinada média e variância.</span><span class="sxs-lookup"><span data-stu-id="5e0eb-105">Returns a normal distribution with a given mean and variance.</span></span>

```qsharp
function NormalDistribution (mean : Double, variance : Double) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a><span data-ttu-id="5e0eb-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="5e0eb-106">Input</span></span>

### <a name="mean--double"></a><span data-ttu-id="5e0eb-107">média: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5e0eb-107">mean : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>




### <a name="variance--double"></a><span data-ttu-id="5e0eb-108">variância: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5e0eb-108">variance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>





## <a name="output--continuousdistribution"></a><span data-ttu-id="5e0eb-109">Saída: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="5e0eb-109">Output : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>



## <a name="example"></a><span data-ttu-id="5e0eb-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="5e0eb-110">Example</span></span>

<span data-ttu-id="5e0eb-111">O seguinte desenha 10 amostras da distribuição normal com média 2 e desvio padrão 0,1:</span><span class="sxs-lookup"><span data-stu-id="5e0eb-111">The following draws 10 samples from the normal distribution with mean 2 and standard deviation 0.1:</span></span>

```qsharp
let samples = DrawMany(
    (NormalDistribution(2.0, PowD(0.1, 2.0)))::Sample,
    10, ()
);
```

## <a name="see-also"></a><span data-ttu-id="5e0eb-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="5e0eb-112">See Also</span></span>

- [<span data-ttu-id="5e0eb-113">Microsoft. Quantum. Random. StandardNormalDistribution</span><span class="sxs-lookup"><span data-stu-id="5e0eb-113">Microsoft.Quantum.Random.StandardNormalDistribution</span></span>](xref:Microsoft.Quantum.Random.StandardNormalDistribution)