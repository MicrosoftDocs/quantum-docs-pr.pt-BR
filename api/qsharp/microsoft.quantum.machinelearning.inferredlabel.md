---
uid: Microsoft.Quantum.MachineLearning.InferredLabel
title: Função InferredLabel
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabel
qsharp.summary: Given a of classification probability and a bias, returns the label inferred from that probability.
ms.openlocfilehash: 1d6edec94f731fe96da797f0c3d77e6eba565149
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694998"
---
# <a name="inferredlabel-function"></a><span data-ttu-id="8441a-102">Função InferredLabel</span><span class="sxs-lookup"><span data-stu-id="8441a-102">InferredLabel function</span></span>

<span data-ttu-id="8441a-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="8441a-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="8441a-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8441a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8441a-105">Devido a uma probabilidade de classificação e uma tendência, retorna o rótulo inferido da probabilidade.</span><span class="sxs-lookup"><span data-stu-id="8441a-105">Given a of classification probability and a bias, returns the label inferred from that probability.</span></span>

```qsharp
function InferredLabel (bias : Double, probability : Double) : Int
```


## <a name="input"></a><span data-ttu-id="8441a-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="8441a-106">Input</span></span>

### <a name="bias--double"></a><span data-ttu-id="8441a-107">tendência: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8441a-107">bias : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8441a-108">A tendência entre duas classes, geralmente o resultado do treinamento de um classificador.</span><span class="sxs-lookup"><span data-stu-id="8441a-108">The bias between two classes, typically the result of training a classifier.</span></span>


### <a name="probability--double"></a><span data-ttu-id="8441a-109">probabilidade: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8441a-109">probability : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8441a-110">As probabilidades de classificação para um exemplo específico, normalmente resultando da estimativa da sua frequência de classificação.</span><span class="sxs-lookup"><span data-stu-id="8441a-110">A classification probabilities for a particular sample, typically resulting from estimating its classification frequency.</span></span>



## <a name="output--int"></a><span data-ttu-id="8441a-111">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8441a-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8441a-112">O rótulo inferido da probabilidade de classificação fornecida.</span><span class="sxs-lookup"><span data-stu-id="8441a-112">The label inferred from the given classification probability.</span></span>