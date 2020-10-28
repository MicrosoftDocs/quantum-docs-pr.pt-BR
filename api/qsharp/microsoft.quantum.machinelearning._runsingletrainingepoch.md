---
uid: Microsoft.Quantum.MachineLearning._RunSingleTrainingEpoch
title: _RunSingleTrainingEpoch operação
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: _RunSingleTrainingEpoch
qsharp.summary: Perform one epoch of sequential classifier training on a subset of data samples.
ms.openlocfilehash: 2b4f629eac0bd8e60bd4d86077521c60085d4809
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694703"
---
# <a name="_runsingletrainingepoch-operation"></a><span data-ttu-id="ab28e-102">_RunSingleTrainingEpoch operação</span><span class="sxs-lookup"><span data-stu-id="ab28e-102">_RunSingleTrainingEpoch operation</span></span>

<span data-ttu-id="ab28e-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="ab28e-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="ab28e-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ab28e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ab28e-105">Execute uma época de treinamento sequencial de classificador em um subconjunto de exemplos de dados.</span><span class="sxs-lookup"><span data-stu-id="ab28e-105">Perform one epoch of sequential classifier training on a subset of data samples.</span></span>

```qsharp
operation _RunSingleTrainingEpoch (encodedSamples : (Microsoft.Quantum.MachineLearning.LabeledSample, Microsoft.Quantum.MachineLearning.StateGenerator)[], schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, periodScore : Int, options : Microsoft.Quantum.MachineLearning.TrainingOptions, model : Microsoft.Quantum.MachineLearning.SequentialModel, nPreviousBestMisses : Int) : (Int, Microsoft.Quantum.MachineLearning.SequentialModel)
```


## <a name="input"></a><span data-ttu-id="ab28e-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="ab28e-106">Input</span></span>

### <a name="encodedsamples--labeledsamplestategenerator"></a><span data-ttu-id="ab28e-107">encodedSamples: ([LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample),[StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)) []</span><span class="sxs-lookup"><span data-stu-id="ab28e-107">encodedSamples : ([LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample),[StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator))[]</span></span>




### <a name="schedule--samplingschedule"></a><span data-ttu-id="ab28e-108">agendamento: [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="ab28e-108">schedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>




### <a name="periodscore--int"></a><span data-ttu-id="ab28e-109">periodScore: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ab28e-109">periodScore : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ab28e-110">O número de etapas de gradiente a serem seguidas entre pontos de pontuação.</span><span class="sxs-lookup"><span data-stu-id="ab28e-110">The number of gradient steps to be taken between scoring points.</span></span>
<span data-ttu-id="ab28e-111">Para obter a melhor precisão, defina como 1.</span><span class="sxs-lookup"><span data-stu-id="ab28e-111">For best accuracy, set to 1.</span></span>


### <a name="options--trainingoptions"></a><span data-ttu-id="ab28e-112">opções: [trainoptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span><span class="sxs-lookup"><span data-stu-id="ab28e-112">options : [TrainingOptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span></span>

<span data-ttu-id="ab28e-113">Opções a serem usadas no treinamento.</span><span class="sxs-lookup"><span data-stu-id="ab28e-113">Options to be used in training.</span></span>


### <a name="model--sequentialmodel"></a><span data-ttu-id="ab28e-114">modelo: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="ab28e-114">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="ab28e-115">O modelo sequencial a ser treinado.</span><span class="sxs-lookup"><span data-stu-id="ab28e-115">The sequential model to be trained.</span></span>


### <a name="npreviousbestmisses--int"></a><span data-ttu-id="ab28e-116">nPreviousBestMisses: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ab28e-116">nPreviousBestMisses : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ab28e-117">O melhor número de classificações incorretas observadas nas épocas anteriores.</span><span class="sxs-lookup"><span data-stu-id="ab28e-117">The best number of misclassifications observed in previous epochs.</span></span>



## <a name="output--intsequentialmodel"></a><span data-ttu-id="ab28e-118">Saída: ([int](xref:microsoft.quantum.lang-ref.int),[SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel))</span><span class="sxs-lookup"><span data-stu-id="ab28e-118">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel))</span></span>

- <span data-ttu-id="ab28e-119">O menor número de classificações incorretas observadas até essa época.</span><span class="sxs-lookup"><span data-stu-id="ab28e-119">The smallest number of misclassifications observed through to this epoch.</span></span>
- <span data-ttu-id="ab28e-120">O novo modelo melhor sequencial encontrado.</span><span class="sxs-lookup"><span data-stu-id="ab28e-120">The new best sequential model found.</span></span>