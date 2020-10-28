---
uid: Microsoft.Quantum.MachineLearning.InferredLabels
title: Função InferredLabels
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabels
qsharp.summary: Given an array of classification probabilities and a bias, returns the label inferred from each probability.
ms.openlocfilehash: 874d1a2f7cc6d67567e0d2baa70b0d26b639a029
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694993"
---
# <a name="inferredlabels-function"></a><span data-ttu-id="8341d-102">Função InferredLabels</span><span class="sxs-lookup"><span data-stu-id="8341d-102">InferredLabels function</span></span>

<span data-ttu-id="8341d-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="8341d-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="8341d-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8341d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8341d-105">Dada uma matriz de probabilidades de classificação e uma tendência, retorna o rótulo inferido de cada probabilidade.</span><span class="sxs-lookup"><span data-stu-id="8341d-105">Given an array of classification probabilities and a bias, returns the label inferred from each probability.</span></span>

```qsharp
function InferredLabels (bias : Double, probabilities : Double[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="8341d-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="8341d-106">Input</span></span>

### <a name="bias--double"></a><span data-ttu-id="8341d-107">tendência: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8341d-107">bias : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8341d-108">A tendência entre duas classes, geralmente o resultado do treinamento de um classificador.</span><span class="sxs-lookup"><span data-stu-id="8341d-108">The bias between two classes, typically the result of training a classifier.</span></span>


### <a name="probabilities--double"></a><span data-ttu-id="8341d-109">probabilidades: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="8341d-109">probabilities : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="8341d-110">Uma matriz de probabilidades de classificação para um conjunto de amostras, normalmente resultante da estimativa de frequências de classificação.</span><span class="sxs-lookup"><span data-stu-id="8341d-110">An array of classification probabilities for a set of samples, typically resulting from estimating classification frequencies.</span></span>



## <a name="output--int"></a><span data-ttu-id="8341d-111">Saída: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="8341d-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="8341d-112">O rótulo inferido de cada probabilidade de classificação.</span><span class="sxs-lookup"><span data-stu-id="8341d-112">The label inferred from each classification probability.</span></span>