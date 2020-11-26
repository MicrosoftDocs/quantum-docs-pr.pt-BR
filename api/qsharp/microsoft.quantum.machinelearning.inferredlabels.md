---
uid: Microsoft.Quantum.MachineLearning.InferredLabels
title: Função InferredLabels
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabels
qsharp.summary: Given an array of classification probabilities and a bias, returns the label inferred from each probability.
ms.openlocfilehash: 668ab89ed45c49d33ce50ff5d892f4d57246c12a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196354"
---
# <a name="inferredlabels-function"></a><span data-ttu-id="425ad-102">Função InferredLabels</span><span class="sxs-lookup"><span data-stu-id="425ad-102">InferredLabels function</span></span>

<span data-ttu-id="425ad-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="425ad-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="425ad-104">Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="425ad-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="425ad-105">Dada uma matriz de probabilidades de classificação e uma tendência, retorna o rótulo inferido de cada probabilidade.</span><span class="sxs-lookup"><span data-stu-id="425ad-105">Given an array of classification probabilities and a bias, returns the label inferred from each probability.</span></span>

```qsharp
function InferredLabels (bias : Double, probabilities : Double[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="425ad-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="425ad-106">Input</span></span>

### <a name="bias--double"></a><span data-ttu-id="425ad-107">tendência: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="425ad-107">bias : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="425ad-108">A tendência entre duas classes, geralmente o resultado do treinamento de um classificador.</span><span class="sxs-lookup"><span data-stu-id="425ad-108">The bias between two classes, typically the result of training a classifier.</span></span>


### <a name="probabilities--double"></a><span data-ttu-id="425ad-109">probabilidades: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="425ad-109">probabilities : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="425ad-110">Uma matriz de probabilidades de classificação para um conjunto de amostras, normalmente resultante da estimativa de frequências de classificação.</span><span class="sxs-lookup"><span data-stu-id="425ad-110">An array of classification probabilities for a set of samples, typically resulting from estimating classification frequencies.</span></span>



## <a name="output--int"></a><span data-ttu-id="425ad-111">Saída: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="425ad-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="425ad-112">O rótulo inferido de cada probabilidade de classificação.</span><span class="sxs-lookup"><span data-stu-id="425ad-112">The label inferred from each classification probability.</span></span>