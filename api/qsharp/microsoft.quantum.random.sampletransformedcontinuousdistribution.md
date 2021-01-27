---
uid: Microsoft.Quantum.Random.SampleTransformedContinuousDistribution
title: Operação SampleTransformedContinuousDistribution
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: SampleTransformedContinuousDistribution
qsharp.summary: Internal-only operation for sampling from transformed distributions. Should only be used via partial application.
ms.openlocfilehash: 62f6f4ff372143228de007c98a23697022fcfd24
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856094"
---
# <a name="sampletransformedcontinuousdistribution-operation"></a><span data-ttu-id="10d43-102">Operação SampleTransformedContinuousDistribution</span><span class="sxs-lookup"><span data-stu-id="10d43-102">SampleTransformedContinuousDistribution operation</span></span>

<span data-ttu-id="10d43-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="10d43-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="10d43-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="10d43-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="10d43-105">Operação somente interna para amostragem de distribuições transformadas.</span><span class="sxs-lookup"><span data-stu-id="10d43-105">Internal-only operation for sampling from transformed distributions.</span></span>
<span data-ttu-id="10d43-106">Só deve ser usado por meio de aplicativo parcial.</span><span class="sxs-lookup"><span data-stu-id="10d43-106">Should only be used via partial application.</span></span>

```qsharp
operation SampleTransformedContinuousDistribution (transform : (Double -> Double), distribution : Microsoft.Quantum.Random.ContinuousDistribution) : Double
```


## <a name="input"></a><span data-ttu-id="10d43-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="10d43-107">Input</span></span>

### <a name="transform--double---double"></a><span data-ttu-id="10d43-108">transformação: [duplo](xref:microsoft.quantum.lang-ref.double) -> [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="10d43-108">transform : [Double](xref:microsoft.quantum.lang-ref.double) -> [Double](xref:microsoft.quantum.lang-ref.double)</span></span>




### <a name="distribution--continuousdistribution"></a><span data-ttu-id="10d43-109">distribuição: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="10d43-109">distribution : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>





## <a name="output--double"></a><span data-ttu-id="10d43-110">Saída: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="10d43-110">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

