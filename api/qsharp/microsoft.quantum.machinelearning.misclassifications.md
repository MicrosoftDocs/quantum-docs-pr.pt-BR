---
uid: Microsoft.Quantum.MachineLearning.Misclassifications
title: Função de classificações incorretas
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Misclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns indices for where each set of labels differs.
ms.openlocfilehash: e13a9b9b65931678d5d87878e81fa172329a28ea
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211671"
---
# <a name="misclassifications-function"></a><span data-ttu-id="61889-102">Função de classificações incorretas</span><span class="sxs-lookup"><span data-stu-id="61889-102">Misclassifications function</span></span>

<span data-ttu-id="61889-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="61889-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="61889-104">Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="61889-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="61889-105">Dado um conjunto de rótulos deduzidos e um conjunto de rótulos corretos, retorna índices para onde cada conjunto de rótulos difere.</span><span class="sxs-lookup"><span data-stu-id="61889-105">Given a set of inferred labels and a set of correct labels, returns indices for where each set of labels differs.</span></span>

```qsharp
function Misclassifications (inferredLabels : Int[], actualLabels : Int[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="61889-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="61889-106">Input</span></span>

### <a name="inferredlabels--int"></a><span data-ttu-id="61889-107">inferredLabels: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="61889-107">inferredLabels : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="61889-108">Os rótulos inferidos para um determinado treinamento ou conjunto de validação.</span><span class="sxs-lookup"><span data-stu-id="61889-108">The labels inferred for a given training or validation set.</span></span>


### <a name="actuallabels--int"></a><span data-ttu-id="61889-109">actualLabels: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="61889-109">actualLabels : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="61889-110">Os rótulos verdadeiros para um determinado treinamento ou conjunto de validação.</span><span class="sxs-lookup"><span data-stu-id="61889-110">The true labels for a given training or validation set.</span></span>



## <a name="output--int"></a><span data-ttu-id="61889-111">Saída: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="61889-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="61889-112">Uma matriz de índices `idx` como essa `inferredLabels[idx] != actualLabels[idx]` .</span><span class="sxs-lookup"><span data-stu-id="61889-112">An array of indices `idx` such that `inferredLabels[idx] != actualLabels[idx]`.</span></span>