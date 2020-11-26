---
uid: Microsoft.Quantum.MachineLearning.EstimateClassificationProbabilities
title: Operação EstimateClassificationProbabilities
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateClassificationProbabilities
qsharp.summary: Given a set of samples and a sequential classifier, estimates the classification probability for those samples by repeatedly measuring the output of the classifier on each sample.
ms.openlocfilehash: 1cd56f6a6483b00afb168f8d84301e73eae9af65
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211892"
---
# <a name="estimateclassificationprobabilities-operation"></a><span data-ttu-id="89762-102">Operação EstimateClassificationProbabilities</span><span class="sxs-lookup"><span data-stu-id="89762-102">EstimateClassificationProbabilities operation</span></span>

<span data-ttu-id="89762-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="89762-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="89762-104">Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="89762-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="89762-105">Dado um conjunto de amostras e um classificador sequencial, o estima a probabilidade de classificação para esses exemplos medindo repetidamente a saída do classificador em cada amostra.</span><span class="sxs-lookup"><span data-stu-id="89762-105">Given a set of samples and a sequential classifier, estimates the classification probability for those samples by repeatedly measuring the output of the classifier on each sample.</span></span>

```qsharp
operation EstimateClassificationProbabilities (tolerance : Double, model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Double[][], nMeasurements : Int) : Double[]
```


## <a name="input"></a><span data-ttu-id="89762-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="89762-106">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="89762-107">tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="89762-107">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="89762-108">A tolerância para permitir a codificação da amostra em uma operação de preparação de estado.</span><span class="sxs-lookup"><span data-stu-id="89762-108">The tolerance to allow in encoding the sample into a state preparation operation.</span></span>


### <a name="model--sequentialmodel"></a><span data-ttu-id="89762-109">modelo: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="89762-109">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="89762-110">O modelo sequencial a ser usado para estimar as probabilidades de classificação para os exemplos fornecidos.</span><span class="sxs-lookup"><span data-stu-id="89762-110">The sequential model to be used to estimate the classification probabilities for the given samples.</span></span>


### <a name="samples--double"></a><span data-ttu-id="89762-111">exemplos: [Double](xref:microsoft.quantum.lang-ref.double)[] []</span><span class="sxs-lookup"><span data-stu-id="89762-111">samples : [Double](xref:microsoft.quantum.lang-ref.double)[][]</span></span>

<span data-ttu-id="89762-112">Uma matriz de vetores de recurso para cada amostra a ser classificada.</span><span class="sxs-lookup"><span data-stu-id="89762-112">An array of feature vectors for each sample to be classified.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="89762-113">nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="89762-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="89762-114">O número de medições a serem usadas na estimativa da probabilidade de classificação.</span><span class="sxs-lookup"><span data-stu-id="89762-114">The number of measurements to use in estimating the classification probability.</span></span>



## <a name="output--double"></a><span data-ttu-id="89762-115">Saída: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="89762-115">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="89762-116">Uma matriz de estimativas da probabilidade de classificação para cada amostra fornecida.</span><span class="sxs-lookup"><span data-stu-id="89762-116">An array of estimates of the classification probability for each given sample.</span></span>