---
uid: Microsoft.Quantum.MachineLearning.NQubitsRequired
title: Função NQubitsRequired
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: NQubitsRequired
qsharp.summary: Returns the number of qubits required to apply a given sequential classifier.
ms.openlocfilehash: d7ed687e9c75ed7cc71917aa1cdf32a6fbb93106
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696819"
---
# <a name="nqubitsrequired-function"></a><span data-ttu-id="b80f2-102">Função NQubitsRequired</span><span class="sxs-lookup"><span data-stu-id="b80f2-102">NQubitsRequired function</span></span>

<span data-ttu-id="b80f2-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="b80f2-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="b80f2-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b80f2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b80f2-105">Retorna o número de qubits necessário para aplicar um classificador sequencial fornecido.</span><span class="sxs-lookup"><span data-stu-id="b80f2-105">Returns the number of qubits required to apply a given sequential classifier.</span></span>

```qsharp
function NQubitsRequired (model : Microsoft.Quantum.MachineLearning.SequentialModel) : Int
```


## <a name="input"></a><span data-ttu-id="b80f2-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="b80f2-106">Input</span></span>

### <a name="model--sequentialmodel"></a><span data-ttu-id="b80f2-107">modelo: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="b80f2-107">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>





## <a name="output--int"></a><span data-ttu-id="b80f2-108">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b80f2-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b80f2-109">O tamanho mínimo de um registro no qual o classificador sequencial pode ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="b80f2-109">The minimum size of a register on which the sequential classifier may be applied.</span></span>