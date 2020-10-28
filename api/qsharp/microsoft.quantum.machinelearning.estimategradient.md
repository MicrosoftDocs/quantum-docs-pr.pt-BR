---
uid: Microsoft.Quantum.MachineLearning.EstimateGradient
title: Operação EstimateGradient
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateGradient
qsharp.summary: Estimates the training gradient for a sequential classifier at a particular model and for a given encoded input.
ms.openlocfilehash: f42cc30c98346a25f584d7527227a95cb413c32b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694593"
---
# <a name="estimategradient-operation"></a><span data-ttu-id="8459e-102">Operação EstimateGradient</span><span class="sxs-lookup"><span data-stu-id="8459e-102">EstimateGradient operation</span></span>

<span data-ttu-id="8459e-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="8459e-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="8459e-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8459e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8459e-105">Estima o gradiente de treinamento para um classificador sequencial em um modelo específico e para uma determinada entrada codificada.</span><span class="sxs-lookup"><span data-stu-id="8459e-105">Estimates the training gradient for a sequential classifier at a particular model and for a given encoded input.</span></span>

```qsharp
operation EstimateGradient (model : Microsoft.Quantum.MachineLearning.SequentialModel, encodedInput : Microsoft.Quantum.MachineLearning.StateGenerator, nMeasurements : Int) : Double[]
```


## <a name="input"></a><span data-ttu-id="8459e-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="8459e-106">Input</span></span>

### <a name="model--sequentialmodel"></a><span data-ttu-id="8459e-107">modelo: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="8459e-107">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="8459e-108">O modelo sequencial cujo gradiente deve ser estimado.</span><span class="sxs-lookup"><span data-stu-id="8459e-108">The sequential model whose gradient is to be estimated.</span></span>


### <a name="encodedinput--stategenerator"></a><span data-ttu-id="8459e-109">encodedInput: [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span><span class="sxs-lookup"><span data-stu-id="8459e-109">encodedInput : [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span></span>

<span data-ttu-id="8459e-110">Uma entrada para o classificador sequencial, codificada em uma operação de preparação de estado.</span><span class="sxs-lookup"><span data-stu-id="8459e-110">An input to the sequential classifier, encoded into a state preparation operation.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="8459e-111">nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8459e-111">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8459e-112">O número de medições a serem usadas na estimativa do gradiente.</span><span class="sxs-lookup"><span data-stu-id="8459e-112">The number of measurements to use in estimating the gradient.</span></span>



## <a name="output--double"></a><span data-ttu-id="8459e-113">Saída: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="8459e-113">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="8459e-114">Uma estimativa do gradiente de treinamento nos parâmetros de entrada e modelo especificados.</span><span class="sxs-lookup"><span data-stu-id="8459e-114">An estimate of the training gradient at the given input and model parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="8459e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="8459e-115">Remarks</span></span>

<span data-ttu-id="8459e-116">Essa operação usa um teste Hadamard e a técnica Shift de parâmetro em conjunto para estimar o gradiente.</span><span class="sxs-lookup"><span data-stu-id="8459e-116">This operation uses a Hadamard test and the parameter shift technique together to estimate the gradient.</span></span>