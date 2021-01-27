---
uid: Microsoft.Quantum.MachineLearning.Misclassifications
title: Função de classificações incorretas
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Misclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns indices for where each set of labels differs.
ms.openlocfilehash: 3913395fbd9f7cf96732c17ca0c726289e5087ed
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853919"
---
# <a name="misclassifications-function"></a><span data-ttu-id="80dee-102">Função de classificações incorretas</span><span class="sxs-lookup"><span data-stu-id="80dee-102">Misclassifications function</span></span>

<span data-ttu-id="80dee-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="80dee-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="80dee-104">Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="80dee-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="80dee-105">Dado um conjunto de rótulos deduzidos e um conjunto de rótulos corretos, retorna índices para onde cada conjunto de rótulos difere.</span><span class="sxs-lookup"><span data-stu-id="80dee-105">Given a set of inferred labels and a set of correct labels, returns indices for where each set of labels differs.</span></span>

```qsharp
function Misclassifications (inferredLabels : Int[], actualLabels : Int[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="80dee-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="80dee-106">Input</span></span>

### <a name="inferredlabels--int"></a><span data-ttu-id="80dee-107">inferredLabels: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="80dee-107">inferredLabels : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="80dee-108">Os rótulos inferidos para um determinado treinamento ou conjunto de validação.</span><span class="sxs-lookup"><span data-stu-id="80dee-108">The labels inferred for a given training or validation set.</span></span>


### <a name="actuallabels--int"></a><span data-ttu-id="80dee-109">actualLabels: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="80dee-109">actualLabels : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="80dee-110">Os rótulos verdadeiros para um determinado treinamento ou conjunto de validação.</span><span class="sxs-lookup"><span data-stu-id="80dee-110">The true labels for a given training or validation set.</span></span>



## <a name="output--int"></a><span data-ttu-id="80dee-111">Saída: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="80dee-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="80dee-112">Uma matriz de índices `idx` como essa `inferredLabels[idx] != actualLabels[idx]` .</span><span class="sxs-lookup"><span data-stu-id="80dee-112">An array of indices `idx` such that `inferredLabels[idx] != actualLabels[idx]`.</span></span>

## <a name="example"></a><span data-ttu-id="80dee-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="80dee-113">Example</span></span>

```qsharp
let misclassifications = Misclassifications([0, 1, 0, 0], [0, 1, 1, 0]);
Message($"{misclassifications}"); // Will print [2].
```