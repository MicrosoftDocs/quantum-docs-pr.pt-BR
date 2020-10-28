---
uid: Microsoft.Quantum.MachineLearning.Misclassifications
title: Função de classificações incorretas
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Misclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns indices for where each set of labels differs.
ms.openlocfilehash: 500c2910f7c5616c88ff6c70ab3cc16680e199fb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696820"
---
# <a name="misclassifications-function"></a><span data-ttu-id="6a3b0-102">Função de classificações incorretas</span><span class="sxs-lookup"><span data-stu-id="6a3b0-102">Misclassifications function</span></span>

<span data-ttu-id="6a3b0-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="6a3b0-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="6a3b0-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6a3b0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6a3b0-105">Dado um conjunto de rótulos deduzidos e um conjunto de rótulos corretos, retorna índices para onde cada conjunto de rótulos difere.</span><span class="sxs-lookup"><span data-stu-id="6a3b0-105">Given a set of inferred labels and a set of correct labels, returns indices for where each set of labels differs.</span></span>

```qsharp
function Misclassifications (inferredLabels : Int[], actualLabels : Int[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="6a3b0-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="6a3b0-106">Input</span></span>

### <a name="inferredlabels--int"></a><span data-ttu-id="6a3b0-107">inferredLabels: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="6a3b0-107">inferredLabels : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="6a3b0-108">Os rótulos inferidos para um determinado treinamento ou conjunto de validação.</span><span class="sxs-lookup"><span data-stu-id="6a3b0-108">The labels inferred for a given training or validation set.</span></span>


### <a name="actuallabels--int"></a><span data-ttu-id="6a3b0-109">actualLabels: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="6a3b0-109">actualLabels : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="6a3b0-110">Os rótulos verdadeiros para um determinado treinamento ou conjunto de validação.</span><span class="sxs-lookup"><span data-stu-id="6a3b0-110">The true labels for a given training or validation set.</span></span>



## <a name="output--int"></a><span data-ttu-id="6a3b0-111">Saída: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="6a3b0-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="6a3b0-112">Uma matriz de índices `idx` como essa `inferredLabels[idx] != actualLabels[idx]` .</span><span class="sxs-lookup"><span data-stu-id="6a3b0-112">An array of indices `idx` such that `inferredLabels[idx] != actualLabels[idx]`.</span></span>