---
uid: Microsoft.Quantum.Random.StandardNormalDistribution
title: Função StandardNormalDistribution
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: StandardNormalDistribution
qsharp.summary: Returns a normal distribution with mean 0 and variance 1.
ms.openlocfilehash: e1776339655c33516f7b3d156f1b377a0c74d250
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857810"
---
# <a name="standardnormaldistribution-function"></a><span data-ttu-id="05e77-102">Função StandardNormalDistribution</span><span class="sxs-lookup"><span data-stu-id="05e77-102">StandardNormalDistribution function</span></span>

<span data-ttu-id="05e77-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="05e77-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="05e77-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="05e77-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="05e77-105">Retorna uma distribuição normal com média 0 e variância 1.</span><span class="sxs-lookup"><span data-stu-id="05e77-105">Returns a normal distribution with mean 0 and variance 1.</span></span>

```qsharp
function StandardNormalDistribution () : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="output--continuousdistribution"></a><span data-ttu-id="05e77-106">Saída: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="05e77-106">Output : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>



## <a name="example"></a><span data-ttu-id="05e77-107">Exemplo</span><span class="sxs-lookup"><span data-stu-id="05e77-107">Example</span></span>

<span data-ttu-id="05e77-108">O seguinte desenha 10 exemplos da distribuição normal padrão:</span><span class="sxs-lookup"><span data-stu-id="05e77-108">The following draws 10 samples from the standard normal distribution:</span></span>

```qsharp
let samples = DrawMany((StandardNormalDistribution())::Sample, 10, ());
```

## <a name="see-also"></a><span data-ttu-id="05e77-109">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="05e77-109">See Also</span></span>

- [<span data-ttu-id="05e77-110">Microsoft. Quantum. Random. NormalDistribution</span><span class="sxs-lookup"><span data-stu-id="05e77-110">Microsoft.Quantum.Random.NormalDistribution</span></span>](xref:Microsoft.Quantum.Random.NormalDistribution)