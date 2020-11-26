---
uid: Microsoft.Quantum.MachineLearning.TrainingOptions
title: Tipo definido pelo usuário trainoptions
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: TrainingOptions
qsharp.summary: A collection of options to be used in training quantum classifiers.
ms.openlocfilehash: 280a3857aa7bc42f636a33f893d4f450e79b6a6a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196116"
---
# <a name="trainingoptions-user-defined-type"></a><span data-ttu-id="88210-102">Tipo definido pelo usuário trainoptions</span><span class="sxs-lookup"><span data-stu-id="88210-102">TrainingOptions user defined type</span></span>

<span data-ttu-id="88210-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="88210-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="88210-104">Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="88210-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="88210-105">Uma coleção de opções a ser usada em classificadores do quantum de treinamento.</span><span class="sxs-lookup"><span data-stu-id="88210-105">A collection of options to be used in training quantum classifiers.</span></span>

```qsharp

newtype TrainingOptions = (LearningRate : Double, Tolerance : Double, MinibatchSize : Int, NMeasurements : Int, MaxEpochs : Int, MaxStalls : Int, StochasticRescaleFactor : Double, ScoringPeriod : Int, VerboseMessage : (String -> Unit));
```



## <a name="named-items"></a><span data-ttu-id="88210-106">Itens nomeados</span><span class="sxs-lookup"><span data-stu-id="88210-106">Named Items</span></span>

### <a name="learningrate--double"></a><span data-ttu-id="88210-107">LearningRate: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="88210-107">LearningRate : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="88210-108">A taxa de aprendizagem pela qual os gradientes devem ser redimensionados ao atualizar os parâmetros do modelo durante as etapas de treinamento.</span><span class="sxs-lookup"><span data-stu-id="88210-108">The learning rate by which gradients should be rescaled when updating model parameters during training steps.</span></span>
### <a name="tolerance--double"></a><span data-ttu-id="88210-109">Tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="88210-109">Tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="88210-110">A tolerância a aproximação a ser usada ao preparar exemplos como Estados de Quantum.</span><span class="sxs-lookup"><span data-stu-id="88210-110">The approximation tolerance to use when preparing samples as quantum states.</span></span>
### <a name="minibatchsize--int"></a><span data-ttu-id="88210-111">MinibatchSize: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="88210-111">MinibatchSize : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="88210-112">O número de amostras a serem usadas em cada minilote de treinamento.</span><span class="sxs-lookup"><span data-stu-id="88210-112">The number of samples to use in each training minibatch.</span></span>
### <a name="nmeasurements--int"></a><span data-ttu-id="88210-113">NMeasurements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="88210-113">NMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="88210-114">O número de vezes para medir cada resultado de classificação a fim de estimar a probabilidade de classificação.</span><span class="sxs-lookup"><span data-stu-id="88210-114">The number of times to measure each classification result in order to estimate the classification probability.</span></span>
### <a name="maxepochs--int"></a><span data-ttu-id="88210-115">MaxEpochs: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="88210-115">MaxEpochs : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="88210-116">O número máximo de épocas para treinar cada modelo.</span><span class="sxs-lookup"><span data-stu-id="88210-116">The maximum number of epochs to train each model for.</span></span>
### <a name="maxstalls--int"></a><span data-ttu-id="88210-117">MaxStalls: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="88210-117">MaxStalls : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="88210-118">O número máximo de vezes que uma época de treinamento tem permissão para paralisar (aproximadamente zero gradiente) antes de falhar.</span><span class="sxs-lookup"><span data-stu-id="88210-118">The maximum number of times a training epoch is allowed to stall (approximately zero gradient) before failing.</span></span>
### <a name="stochasticrescalefactor--double"></a><span data-ttu-id="88210-119">StochasticRescaleFactor: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="88210-119">StochasticRescaleFactor : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="88210-120">O valor para redimensionar os modelos interrompidos antes de tentar novamente uma atualização.</span><span class="sxs-lookup"><span data-stu-id="88210-120">The amount to rescale stalled models by before retrying an update.</span></span>
### <a name="scoringperiod--int"></a><span data-ttu-id="88210-121">ScoringPeriod: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="88210-121">ScoringPeriod : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="88210-122">O número de etapas de gradiente a serem seguidas entre pontos de pontuação.</span><span class="sxs-lookup"><span data-stu-id="88210-122">The number of gradient steps to be taken between scoring points.</span></span>
<span data-ttu-id="88210-123">Para obter a melhor precisão, defina como 1.</span><span class="sxs-lookup"><span data-stu-id="88210-123">For best accuracy, set to 1.</span></span>
### <a name="verbosemessage--string---unit"></a><span data-ttu-id="88210-124">VerboseMessage: unidade de [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string) -> [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="88210-124">VerboseMessage : [String](xref:microsoft.quantum.lang-ref.string) -> [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="88210-125">Uma função que pode ser usada para fornecer comentários detalhados.</span><span class="sxs-lookup"><span data-stu-id="88210-125">A function that can be used to provide verbose feedback.</span></span>

## <a name="remarks"></a><span data-ttu-id="88210-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="88210-126">Remarks</span></span>

<span data-ttu-id="88210-127">Esse UDT não deve ser criado diretamente, mas deve ser especificado chamando @"microsoft.quantum.machinelearning.defaulttrainingoptions" e, em seguida, usando o `w/` operador para substituir os padrões diferentes.</span><span class="sxs-lookup"><span data-stu-id="88210-127">This UDT should not be created directly, but rather should be specified by calling @"microsoft.quantum.machinelearning.defaulttrainingoptions" and then using the `w/` operator to override different defaults.</span></span>

<span data-ttu-id="88210-128">Por exemplo, para usar medidas de 100.000 e no máximo 8 épocas de treinamento:</span><span class="sxs-lookup"><span data-stu-id="88210-128">For example, to use 100,000 measurements and at most 8 training epochs:</span></span>

```Q#
let options = DefaultTrainingOptions()
              w/ NMeasurements <- 100000
              w/ MaxEpochs <- 8;
```

## <a name="references"></a><span data-ttu-id="88210-129">Referências</span><span class="sxs-lookup"><span data-stu-id="88210-129">References</span></span>

- [<span data-ttu-id="88210-130">arXiv:1804.00633</span><span class="sxs-lookup"><span data-stu-id="88210-130">arXiv:1804.00633</span></span>](https://arxiv.org/abs/1804.00633)