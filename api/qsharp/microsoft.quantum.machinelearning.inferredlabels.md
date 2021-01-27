---
uid: Microsoft.Quantum.MachineLearning.InferredLabels
title: Função InferredLabels
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabels
qsharp.summary: Given an array of classification probabilities and a bias, returns the label inferred from each probability.
ms.openlocfilehash: 576b4b1f11fc21476bbb019d4b0326981294528c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848401"
---
# <a name="inferredlabels-function"></a><span data-ttu-id="ac226-102">Função InferredLabels</span><span class="sxs-lookup"><span data-stu-id="ac226-102">InferredLabels function</span></span>

<span data-ttu-id="ac226-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="ac226-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="ac226-104">Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="ac226-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="ac226-105">Dada uma matriz de probabilidades de classificação e uma tendência, retorna o rótulo inferido de cada probabilidade.</span><span class="sxs-lookup"><span data-stu-id="ac226-105">Given an array of classification probabilities and a bias, returns the label inferred from each probability.</span></span>

```qsharp
function InferredLabels (bias : Double, probabilities : Double[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="ac226-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="ac226-106">Input</span></span>

### <a name="bias--double"></a><span data-ttu-id="ac226-107">tendência: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ac226-107">bias : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ac226-108">A tendência entre duas classes, geralmente o resultado do treinamento de um classificador.</span><span class="sxs-lookup"><span data-stu-id="ac226-108">The bias between two classes, typically the result of training a classifier.</span></span>


### <a name="probabilities--double"></a><span data-ttu-id="ac226-109">probabilidades: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="ac226-109">probabilities : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="ac226-110">Uma matriz de probabilidades de classificação para um conjunto de amostras, normalmente resultante da estimativa de frequências de classificação.</span><span class="sxs-lookup"><span data-stu-id="ac226-110">An array of classification probabilities for a set of samples, typically resulting from estimating classification frequencies.</span></span>



## <a name="output--int"></a><span data-ttu-id="ac226-111">Saída: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="ac226-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="ac226-112">O rótulo inferido de cada probabilidade de classificação.</span><span class="sxs-lookup"><span data-stu-id="ac226-112">The label inferred from each classification probability.</span></span>