---
uid: Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier
title: Operação ValidateSequentialClassifier
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ValidateSequentialClassifier
qsharp.summary: Validates a given sequential classifier against a given set of pre-labeled samples.
ms.openlocfilehash: c100c5786b18996ce13067f1c4618cf0189578f5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848971"
---
# <a name="validatesequentialclassifier-operation"></a><span data-ttu-id="5b6bc-102">Operação ValidateSequentialClassifier</span><span class="sxs-lookup"><span data-stu-id="5b6bc-102">ValidateSequentialClassifier operation</span></span>

<span data-ttu-id="5b6bc-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="5b6bc-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="5b6bc-104">Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="5b6bc-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="5b6bc-105">Valida um classificador sequencial fornecido em relação a um determinado conjunto de amostras previamente rotuladas.</span><span class="sxs-lookup"><span data-stu-id="5b6bc-105">Validates a given sequential classifier against a given set of pre-labeled samples.</span></span>

```qsharp
operation ValidateSequentialClassifier (model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Microsoft.Quantum.MachineLearning.LabeledSample[], tolerance : Double, nMeasurements : Int, validationSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : Microsoft.Quantum.MachineLearning.ValidationResults
```


## <a name="input"></a><span data-ttu-id="5b6bc-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="5b6bc-106">Input</span></span>

### <a name="model--sequentialmodel"></a><span data-ttu-id="5b6bc-107">modelo: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="5b6bc-107">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="5b6bc-108">O modelo sequencial a ser validado.</span><span class="sxs-lookup"><span data-stu-id="5b6bc-108">The sequential model to be validated.</span></span>


### <a name="samples--labeledsample"></a><span data-ttu-id="5b6bc-109">exemplos: [LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]</span><span class="sxs-lookup"><span data-stu-id="5b6bc-109">samples : [LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]</span></span>

<span data-ttu-id="5b6bc-110">Os exemplos a serem usados para validar o modelo fornecido.</span><span class="sxs-lookup"><span data-stu-id="5b6bc-110">The samples to be used to validate the given model.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="5b6bc-111">tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5b6bc-111">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5b6bc-112">A tolerância a aproximação a ser usada na codificação de cada amostra como uma entrada para o classificador sequencial.</span><span class="sxs-lookup"><span data-stu-id="5b6bc-112">The approximation tolerance to use in encoding each sample as an input to the sequential classifier.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="5b6bc-113">nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5b6bc-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5b6bc-114">O número de medições a serem usadas na classificação de cada amostra.</span><span class="sxs-lookup"><span data-stu-id="5b6bc-114">The number of measurements to use in classifying each sample.</span></span>


### <a name="validationschedule--samplingschedule"></a><span data-ttu-id="5b6bc-115">validationSchedule: [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="5b6bc-115">validationSchedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="5b6bc-116">O agendamento pelo qual os exemplos devem ser extraídos do conjunto de validação.</span><span class="sxs-lookup"><span data-stu-id="5b6bc-116">The schedule by which samples should be drawn from the validation set.</span></span>



## <a name="output--validationresults"></a><span data-ttu-id="5b6bc-117">Saída: [ValidationResults](xref:Microsoft.Quantum.MachineLearning.ValidationResults)</span><span class="sxs-lookup"><span data-stu-id="5b6bc-117">Output : [ValidationResults](xref:Microsoft.Quantum.MachineLearning.ValidationResults)</span></span>

<span data-ttu-id="5b6bc-118">Os resultados da validação fornecida.</span><span class="sxs-lookup"><span data-stu-id="5b6bc-118">The results of the given validation.</span></span>