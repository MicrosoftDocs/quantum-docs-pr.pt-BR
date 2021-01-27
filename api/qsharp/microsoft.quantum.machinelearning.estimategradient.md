---
uid: Microsoft.Quantum.MachineLearning.EstimateGradient
title: Operação EstimateGradient
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateGradient
qsharp.summary: Estimates the training gradient for a sequential classifier at a particular model and for a given encoded input.
ms.openlocfilehash: 38edcb67e7dcc5d2e971fb507a792937774a702c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844394"
---
# <a name="estimategradient-operation"></a><span data-ttu-id="ea18f-102">Operação EstimateGradient</span><span class="sxs-lookup"><span data-stu-id="ea18f-102">EstimateGradient operation</span></span>

<span data-ttu-id="ea18f-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="ea18f-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="ea18f-104">Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="ea18f-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="ea18f-105">Estima o gradiente de treinamento para um classificador sequencial em um modelo específico e para uma determinada entrada codificada.</span><span class="sxs-lookup"><span data-stu-id="ea18f-105">Estimates the training gradient for a sequential classifier at a particular model and for a given encoded input.</span></span>

```qsharp
operation EstimateGradient (model : Microsoft.Quantum.MachineLearning.SequentialModel, encodedInput : Microsoft.Quantum.MachineLearning.StateGenerator, nMeasurements : Int) : Double[]
```


## <a name="input"></a><span data-ttu-id="ea18f-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="ea18f-106">Input</span></span>

### <a name="model--sequentialmodel"></a><span data-ttu-id="ea18f-107">modelo: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="ea18f-107">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="ea18f-108">O modelo sequencial cujo gradiente deve ser estimado.</span><span class="sxs-lookup"><span data-stu-id="ea18f-108">The sequential model whose gradient is to be estimated.</span></span>


### <a name="encodedinput--stategenerator"></a><span data-ttu-id="ea18f-109">encodedInput: [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span><span class="sxs-lookup"><span data-stu-id="ea18f-109">encodedInput : [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span></span>

<span data-ttu-id="ea18f-110">Uma entrada para o classificador sequencial, codificada em uma operação de preparação de estado.</span><span class="sxs-lookup"><span data-stu-id="ea18f-110">An input to the sequential classifier, encoded into a state preparation operation.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="ea18f-111">nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ea18f-111">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ea18f-112">O número de medições a serem usadas na estimativa do gradiente.</span><span class="sxs-lookup"><span data-stu-id="ea18f-112">The number of measurements to use in estimating the gradient.</span></span>



## <a name="output--double"></a><span data-ttu-id="ea18f-113">Saída: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="ea18f-113">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="ea18f-114">Uma estimativa do gradiente de treinamento nos parâmetros de entrada e modelo especificados.</span><span class="sxs-lookup"><span data-stu-id="ea18f-114">An estimate of the training gradient at the given input and model parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea18f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea18f-115">Remarks</span></span>

<span data-ttu-id="ea18f-116">Essa operação usa um teste Hadamard e a técnica Shift de parâmetro em conjunto para estimar o gradiente.</span><span class="sxs-lookup"><span data-stu-id="ea18f-116">This operation uses a Hadamard test and the parameter shift technique together to estimate the gradient.</span></span>