---
uid: Microsoft.Quantum.MachineLearning.FeatureRegisterSize
title: Função FeatureRegisterSize
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: FeatureRegisterSize
qsharp.summary: Returns the number of qubits required to encode a particular feature vector.
ms.openlocfilehash: 2754e901d74175c1841a38d795f5de02dabc9b8d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848436"
---
# <a name="featureregistersize-function"></a><span data-ttu-id="9a73b-102">Função FeatureRegisterSize</span><span class="sxs-lookup"><span data-stu-id="9a73b-102">FeatureRegisterSize function</span></span>

<span data-ttu-id="9a73b-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="9a73b-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="9a73b-104">Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="9a73b-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="9a73b-105">Retorna o número de qubits necessário para codificar um vetor de recurso específico.</span><span class="sxs-lookup"><span data-stu-id="9a73b-105">Returns the number of qubits required to encode a particular feature vector.</span></span>

```qsharp
function FeatureRegisterSize (sample : Double[]) : Int
```


## <a name="input"></a><span data-ttu-id="9a73b-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="9a73b-106">Input</span></span>

### <a name="sample--double"></a><span data-ttu-id="9a73b-107">exemplo: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="9a73b-107">sample : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="9a73b-108">Um vetor de recurso de exemplo a ser codificado em um registro qubit.</span><span class="sxs-lookup"><span data-stu-id="9a73b-108">A sample feature vector to be encoded into a qubit register.</span></span>



## <a name="output--int"></a><span data-ttu-id="9a73b-109">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9a73b-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9a73b-110">O tamanho necessário para codificar `sample` em um registro qubit, expresso como um número de qubits.</span><span class="sxs-lookup"><span data-stu-id="9a73b-110">The size required to encode `sample` into a qubit register, expressed as a number of qubits.</span></span>