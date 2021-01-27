---
uid: Microsoft.Quantum.MachineLearning.InferredLabel
title: Função InferredLabel
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabel
qsharp.summary: Given a of classification probability and a bias, returns the label inferred from that probability.
ms.openlocfilehash: 46b24c283a01e6ac1c959ee4a6899591ee708ff7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848413"
---
# <a name="inferredlabel-function"></a><span data-ttu-id="2a5cb-102">Função InferredLabel</span><span class="sxs-lookup"><span data-stu-id="2a5cb-102">InferredLabel function</span></span>

<span data-ttu-id="2a5cb-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="2a5cb-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="2a5cb-104">Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="2a5cb-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="2a5cb-105">Devido a uma probabilidade de classificação e uma tendência, retorna o rótulo inferido da probabilidade.</span><span class="sxs-lookup"><span data-stu-id="2a5cb-105">Given a of classification probability and a bias, returns the label inferred from that probability.</span></span>

```qsharp
function InferredLabel (bias : Double, probability : Double) : Int
```


## <a name="input"></a><span data-ttu-id="2a5cb-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="2a5cb-106">Input</span></span>

### <a name="bias--double"></a><span data-ttu-id="2a5cb-107">tendência: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2a5cb-107">bias : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="2a5cb-108">A tendência entre duas classes, geralmente o resultado do treinamento de um classificador.</span><span class="sxs-lookup"><span data-stu-id="2a5cb-108">The bias between two classes, typically the result of training a classifier.</span></span>


### <a name="probability--double"></a><span data-ttu-id="2a5cb-109">probabilidade: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2a5cb-109">probability : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="2a5cb-110">As probabilidades de classificação para um exemplo específico, normalmente resultando da estimativa da sua frequência de classificação.</span><span class="sxs-lookup"><span data-stu-id="2a5cb-110">A classification probabilities for a particular sample, typically resulting from estimating its classification frequency.</span></span>



## <a name="output--int"></a><span data-ttu-id="2a5cb-111">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2a5cb-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2a5cb-112">O rótulo inferido da probabilidade de classificação fornecida.</span><span class="sxs-lookup"><span data-stu-id="2a5cb-112">The label inferred from the given classification probability.</span></span>