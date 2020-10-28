---
uid: Microsoft.Quantum.MachineLearning.EstimateClassificationProbabilities
title: Operação EstimateClassificationProbabilities
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateClassificationProbabilities
qsharp.summary: Given a set of samples and a sequential classifier, estimates the classification probability for those samples by repeatedly measuring the output of the classifier on each sample.
ms.openlocfilehash: 2b7845d39256f718cc3e415207b8a47b24620bdb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693096"
---
# <a name="estimateclassificationprobabilities-operation"></a><span data-ttu-id="2e428-102">Operação EstimateClassificationProbabilities</span><span class="sxs-lookup"><span data-stu-id="2e428-102">EstimateClassificationProbabilities operation</span></span>

<span data-ttu-id="2e428-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="2e428-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="2e428-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2e428-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2e428-105">Dado um conjunto de amostras e um classificador sequencial, o estima a probabilidade de classificação para esses exemplos medindo repetidamente a saída do classificador em cada amostra.</span><span class="sxs-lookup"><span data-stu-id="2e428-105">Given a set of samples and a sequential classifier, estimates the classification probability for those samples by repeatedly measuring the output of the classifier on each sample.</span></span>

```qsharp
operation EstimateClassificationProbabilities (tolerance : Double, model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Double[][], nMeasurements : Int) : Double[]
```


## <a name="input"></a><span data-ttu-id="2e428-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="2e428-106">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="2e428-107">tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2e428-107">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="2e428-108">A tolerância para permitir a codificação da amostra em uma operação de preparação de estado.</span><span class="sxs-lookup"><span data-stu-id="2e428-108">The tolerance to allow in encoding the sample into a state preparation operation.</span></span>


### <a name="model--sequentialmodel"></a><span data-ttu-id="2e428-109">modelo: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="2e428-109">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="2e428-110">O modelo sequencial a ser usado para estimar as probabilidades de classificação para os exemplos fornecidos.</span><span class="sxs-lookup"><span data-stu-id="2e428-110">The sequential model to be used to estimate the classification probabilities for the given samples.</span></span>


### <a name="samples--double"></a><span data-ttu-id="2e428-111">exemplos: [Double](xref:microsoft.quantum.lang-ref.double)[] []</span><span class="sxs-lookup"><span data-stu-id="2e428-111">samples : [Double](xref:microsoft.quantum.lang-ref.double)[][]</span></span>

<span data-ttu-id="2e428-112">Uma matriz de vetores de recurso para cada amostra a ser classificada.</span><span class="sxs-lookup"><span data-stu-id="2e428-112">An array of feature vectors for each sample to be classified.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="2e428-113">nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2e428-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2e428-114">O número de medições a serem usadas na estimativa da probabilidade de classificação.</span><span class="sxs-lookup"><span data-stu-id="2e428-114">The number of measurements to use in estimating the classification probability.</span></span>



## <a name="output--double"></a><span data-ttu-id="2e428-115">Saída: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="2e428-115">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="2e428-116">Uma matriz de estimativas da probabilidade de classificação para cada amostra fornecida.</span><span class="sxs-lookup"><span data-stu-id="2e428-116">An array of estimates of the classification probability for each given sample.</span></span>