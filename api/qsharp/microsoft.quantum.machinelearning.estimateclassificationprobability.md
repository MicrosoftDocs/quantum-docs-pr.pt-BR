---
uid: Microsoft.Quantum.MachineLearning.EstimateClassificationProbability
title: Operação EstimateClassificationProbability
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateClassificationProbability
qsharp.summary: Given a sample and a sequential classifier, estimates the classification probability for that sample by repeatedly measuring the output of the classifier on the given sample.
ms.openlocfilehash: 79e40bc4bc0954dc6742307122609950bf22ec71
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693094"
---
# <a name="estimateclassificationprobability-operation"></a><span data-ttu-id="53be2-102">Operação EstimateClassificationProbability</span><span class="sxs-lookup"><span data-stu-id="53be2-102">EstimateClassificationProbability operation</span></span>

<span data-ttu-id="53be2-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="53be2-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="53be2-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="53be2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="53be2-105">Dada uma amostra e um classificador sequencial, estima a probabilidade de classificação para esse exemplo medindo repetidamente a saída do classificador no exemplo fornecido.</span><span class="sxs-lookup"><span data-stu-id="53be2-105">Given a sample and a sequential classifier, estimates the classification probability for that sample by repeatedly measuring the output of the classifier on the given sample.</span></span>

```qsharp
operation EstimateClassificationProbability (tolerance : Double, model : Microsoft.Quantum.MachineLearning.SequentialModel, sample : Double[], nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="53be2-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="53be2-106">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="53be2-107">tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="53be2-107">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="53be2-108">A tolerância para permitir a codificação da amostra em uma operação de preparação de estado.</span><span class="sxs-lookup"><span data-stu-id="53be2-108">The tolerance to allow in encoding the sample into a state preparation operation.</span></span>


### <a name="model--sequentialmodel"></a><span data-ttu-id="53be2-109">modelo: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="53be2-109">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="53be2-110">O modelo sequencial a ser usado para estimar a probabilidade de classificação para o exemplo fornecido.</span><span class="sxs-lookup"><span data-stu-id="53be2-110">The sequential model to be used to estimate the classification probability for the given sample.</span></span>


### <a name="sample--double"></a><span data-ttu-id="53be2-111">exemplo: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="53be2-111">sample : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="53be2-112">O vetor de recurso para o exemplo a ser classificado.</span><span class="sxs-lookup"><span data-stu-id="53be2-112">The feature vector for the sample to be classified.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="53be2-113">nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="53be2-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="53be2-114">O número de medições a serem usadas na estimativa da probabilidade de classificação.</span><span class="sxs-lookup"><span data-stu-id="53be2-114">The number of measurements to use in estimating the classification probability.</span></span>



## <a name="output--double"></a><span data-ttu-id="53be2-115">Saída: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="53be2-115">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="53be2-116">Uma estimativa da probabilidade de classificação para o exemplo fornecido.</span><span class="sxs-lookup"><span data-stu-id="53be2-116">An estimate of the classification probability for the given sample.</span></span>