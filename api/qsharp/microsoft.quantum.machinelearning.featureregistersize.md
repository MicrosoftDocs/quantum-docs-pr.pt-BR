---
uid: Microsoft.Quantum.MachineLearning.FeatureRegisterSize
title: Função FeatureRegisterSize
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: FeatureRegisterSize
qsharp.summary: Returns the number of qubits required to encode a particular feature vector.
ms.openlocfilehash: 8f7c47c7547e7a0ac1672f308de445c1b46461e1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696778"
---
# <a name="featureregistersize-function"></a><span data-ttu-id="01293-102">Função FeatureRegisterSize</span><span class="sxs-lookup"><span data-stu-id="01293-102">FeatureRegisterSize function</span></span>

<span data-ttu-id="01293-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="01293-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="01293-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="01293-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="01293-105">Retorna o número de qubits necessário para codificar um vetor de recurso específico.</span><span class="sxs-lookup"><span data-stu-id="01293-105">Returns the number of qubits required to encode a particular feature vector.</span></span>

```qsharp
function FeatureRegisterSize (sample : Double[]) : Int
```


## <a name="input"></a><span data-ttu-id="01293-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="01293-106">Input</span></span>

### <a name="sample--double"></a><span data-ttu-id="01293-107">exemplo: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="01293-107">sample : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="01293-108">Um vetor de recurso de exemplo a ser codificado em um registro qubit.</span><span class="sxs-lookup"><span data-stu-id="01293-108">A sample feature vector to be encoded into a qubit register.</span></span>



## <a name="output--int"></a><span data-ttu-id="01293-109">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="01293-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="01293-110">O tamanho necessário para codificar `sample` em um registro qubit, expresso como um número de qubits.</span><span class="sxs-lookup"><span data-stu-id="01293-110">The size required to encode `sample` into a qubit register, expressed as a number of qubits.</span></span>