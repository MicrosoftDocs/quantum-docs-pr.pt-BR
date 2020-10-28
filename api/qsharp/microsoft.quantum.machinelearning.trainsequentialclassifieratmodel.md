---
uid: Microsoft.Quantum.MachineLearning.TrainSequentialClassifierAtModel
title: Operação TrainSequentialClassifierAtModel
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: TrainSequentialClassifierAtModel
qsharp.summary: Given the structure of a sequential classifier, trains the classifier on a given labeled training set, starting from a particular model.
ms.openlocfilehash: b9e30e4e5bc23f56d9119083045967caff28f13a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694674"
---
# <a name="trainsequentialclassifieratmodel-operation"></a><span data-ttu-id="e025f-102">Operação TrainSequentialClassifierAtModel</span><span class="sxs-lookup"><span data-stu-id="e025f-102">TrainSequentialClassifierAtModel operation</span></span>

<span data-ttu-id="e025f-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="e025f-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="e025f-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e025f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e025f-105">Dada a estrutura de um classificador sequencial, treina o classificador em um determinado conjunto de treinamento rotulado, começando com um modelo específico.</span><span class="sxs-lookup"><span data-stu-id="e025f-105">Given the structure of a sequential classifier, trains the classifier on a given labeled training set, starting from a particular model.</span></span>

```qsharp
operation TrainSequentialClassifierAtModel (model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Microsoft.Quantum.MachineLearning.LabeledSample[], options : Microsoft.Quantum.MachineLearning.TrainingOptions, trainingSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, validationSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : (Microsoft.Quantum.MachineLearning.SequentialModel, Int)
```


## <a name="input"></a><span data-ttu-id="e025f-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="e025f-106">Input</span></span>

### <a name="model--sequentialmodel"></a><span data-ttu-id="e025f-107">modelo: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="e025f-107">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="e025f-108">O modelo sequencial a ser usado como ponto de partida para treinamento.</span><span class="sxs-lookup"><span data-stu-id="e025f-108">The sequential model to be used as a starting point for training.</span></span>


### <a name="samples--labeledsample"></a><span data-ttu-id="e025f-109">exemplos: [LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]</span><span class="sxs-lookup"><span data-stu-id="e025f-109">samples : [LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]</span></span>

<span data-ttu-id="e025f-110">Um conjunto de dados de treinamento rotulados que serão usados para executar o treinamento.</span><span class="sxs-lookup"><span data-stu-id="e025f-110">A set of labeled training data that will be used to perform training.</span></span>


### <a name="options--trainingoptions"></a><span data-ttu-id="e025f-111">opções: [trainoptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span><span class="sxs-lookup"><span data-stu-id="e025f-111">options : [TrainingOptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span></span>

<span data-ttu-id="e025f-112">Configuração a ser usada durante o treinamento; consulte @"microsoft.quantum.machinelearning.trainingoptions" e @"microsoft.quantum.machinelearning.defaulttrainingoptions" para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="e025f-112">Configuration to be used when training; see @"microsoft.quantum.machinelearning.trainingoptions" and @"microsoft.quantum.machinelearning.defaulttrainingoptions" for more details.</span></span>


### <a name="trainingschedule--samplingschedule"></a><span data-ttu-id="e025f-113">trainingSchedule: [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="e025f-113">trainingSchedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="e025f-114">Um agendamento de amostragem a ser usado ao selecionar amostras dos dados de treinamento durante as etapas de treinamento.</span><span class="sxs-lookup"><span data-stu-id="e025f-114">A sampling schedule to use when selecting samples from the training data during training steps.</span></span>


### <a name="validationschedule--samplingschedule"></a><span data-ttu-id="e025f-115">validationSchedule: [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="e025f-115">validationSchedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="e025f-116">Um agendamento de amostragem a ser usado ao selecionar amostras dos dados de treinamento ao selecionar qual ponto inicial resultou na melhor pontuação do classificador.</span><span class="sxs-lookup"><span data-stu-id="e025f-116">A sampling schedule to use when selecting samples from the training data when selecting which start point resulted in the best classifier score.</span></span>



## <a name="output--sequentialmodelint"></a><span data-ttu-id="e025f-117">Saída: ([SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel),[int](xref:microsoft.quantum.lang-ref.int))</span><span class="sxs-lookup"><span data-stu-id="e025f-117">Output : ([SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel),[Int](xref:microsoft.quantum.lang-ref.int))</span></span>

- <span data-ttu-id="e025f-118">Uma parametrização do classificador fornecido e uma tendência entre as duas classes, em conjunto, correspondendo ao melhor resultado de cada um dos pontos de partida fornecidos.</span><span class="sxs-lookup"><span data-stu-id="e025f-118">A parameterization of the given classifier and a bias between the two classes, together corresponding to the best result from each of the given start points.</span></span>
- <span data-ttu-id="e025f-119">O número de erros observados no melhor modelo de classificador.</span><span class="sxs-lookup"><span data-stu-id="e025f-119">The number of misses observed at the best classifier model.</span></span>

## <a name="see-also"></a><span data-ttu-id="e025f-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e025f-120">See Also</span></span>

- [<span data-ttu-id="e025f-121">Microsoft. Quantum. MachineLearning. TrainSequentialClassifier</span><span class="sxs-lookup"><span data-stu-id="e025f-121">Microsoft.Quantum.MachineLearning.TrainSequentialClassifier</span></span>](xref:Microsoft.Quantum.MachineLearning.TrainSequentialClassifier)
- [<span data-ttu-id="e025f-122">Microsoft. Quantum. MachineLearning. ValidateSequentialClassifier</span><span class="sxs-lookup"><span data-stu-id="e025f-122">Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier</span></span>](xref:Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier)