---
uid: Microsoft.Quantum.MachineLearning.EstimateClassificationProbability
title: Operação EstimateClassificationProbability
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateClassificationProbability
qsharp.summary: Given a sample and a sequential classifier, estimates the classification probability for that sample by repeatedly measuring the output of the classifier on the given sample.
ms.openlocfilehash: c2b74bc55ad9005a8f52d05796e856f4f2fb62ba
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853949"
---
# <a name="estimateclassificationprobability-operation"></a><span data-ttu-id="d1d35-102">Operação EstimateClassificationProbability</span><span class="sxs-lookup"><span data-stu-id="d1d35-102">EstimateClassificationProbability operation</span></span>

<span data-ttu-id="d1d35-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="d1d35-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="d1d35-104">Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="d1d35-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="d1d35-105">Dada uma amostra e um classificador sequencial, estima a probabilidade de classificação para esse exemplo medindo repetidamente a saída do classificador no exemplo fornecido.</span><span class="sxs-lookup"><span data-stu-id="d1d35-105">Given a sample and a sequential classifier, estimates the classification probability for that sample by repeatedly measuring the output of the classifier on the given sample.</span></span>

```qsharp
operation EstimateClassificationProbability (tolerance : Double, model : Microsoft.Quantum.MachineLearning.SequentialModel, sample : Double[], nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="d1d35-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="d1d35-106">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="d1d35-107">tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d1d35-107">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d1d35-108">A tolerância para permitir a codificação da amostra em uma operação de preparação de estado.</span><span class="sxs-lookup"><span data-stu-id="d1d35-108">The tolerance to allow in encoding the sample into a state preparation operation.</span></span>


### <a name="model--sequentialmodel"></a><span data-ttu-id="d1d35-109">modelo: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="d1d35-109">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="d1d35-110">O modelo sequencial a ser usado para estimar a probabilidade de classificação para o exemplo fornecido.</span><span class="sxs-lookup"><span data-stu-id="d1d35-110">The sequential model to be used to estimate the classification probability for the given sample.</span></span>


### <a name="sample--double"></a><span data-ttu-id="d1d35-111">exemplo: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="d1d35-111">sample : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="d1d35-112">O vetor de recurso para o exemplo a ser classificado.</span><span class="sxs-lookup"><span data-stu-id="d1d35-112">The feature vector for the sample to be classified.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="d1d35-113">nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d1d35-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d1d35-114">O número de medições a serem usadas na estimativa da probabilidade de classificação.</span><span class="sxs-lookup"><span data-stu-id="d1d35-114">The number of measurements to use in estimating the classification probability.</span></span>



## <a name="output--double"></a><span data-ttu-id="d1d35-115">Saída: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d1d35-115">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d1d35-116">Uma estimativa da probabilidade de classificação para o exemplo fornecido.</span><span class="sxs-lookup"><span data-stu-id="d1d35-116">An estimate of the classification probability for the given sample.</span></span>