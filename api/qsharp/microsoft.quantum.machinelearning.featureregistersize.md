---
uid: Microsoft.Quantum.MachineLearning.FeatureRegisterSize
title: Função FeatureRegisterSize
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: FeatureRegisterSize
qsharp.summary: Returns the number of qubits required to encode a particular feature vector.
ms.openlocfilehash: bc5d5a23cfb431f9506b15bc404ab6955d1c2a35
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196405"
---
# <a name="featureregistersize-function"></a><span data-ttu-id="8f28d-102">Função FeatureRegisterSize</span><span class="sxs-lookup"><span data-stu-id="8f28d-102">FeatureRegisterSize function</span></span>

<span data-ttu-id="8f28d-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="8f28d-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="8f28d-104">Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="8f28d-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="8f28d-105">Retorna o número de qubits necessário para codificar um vetor de recurso específico.</span><span class="sxs-lookup"><span data-stu-id="8f28d-105">Returns the number of qubits required to encode a particular feature vector.</span></span>

```qsharp
function FeatureRegisterSize (sample : Double[]) : Int
```


## <a name="input"></a><span data-ttu-id="8f28d-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="8f28d-106">Input</span></span>

### <a name="sample--double"></a><span data-ttu-id="8f28d-107">exemplo: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="8f28d-107">sample : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="8f28d-108">Um vetor de recurso de exemplo a ser codificado em um registro qubit.</span><span class="sxs-lookup"><span data-stu-id="8f28d-108">A sample feature vector to be encoded into a qubit register.</span></span>



## <a name="output--int"></a><span data-ttu-id="8f28d-109">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8f28d-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8f28d-110">O tamanho necessário para codificar `sample` em um registro qubit, expresso como um número de qubits.</span><span class="sxs-lookup"><span data-stu-id="8f28d-110">The size required to encode `sample` into a qubit register, expressed as a number of qubits.</span></span>