---
uid: Microsoft.Quantum.MachineLearning.PartialRotationsLayer
title: Função PartialRotationsLayer
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: PartialRotationsLayer
qsharp.summary: Returns an array of single-qubit rotations along a given axis, parameterized by distinct model parameters.
ms.openlocfilehash: e230df9b28c59e1d532d5b36adf90efa01f0f33e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852931"
---
# <a name="partialrotationslayer-function"></a><span data-ttu-id="d08b5-102">Função PartialRotationsLayer</span><span class="sxs-lookup"><span data-stu-id="d08b5-102">PartialRotationsLayer function</span></span>

<span data-ttu-id="d08b5-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="d08b5-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="d08b5-104">Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="d08b5-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="d08b5-105">Retorna uma matriz de rotações de qubit único ao longo de um determinado eixo, parametrizado por parâmetros de modelo distintos.</span><span class="sxs-lookup"><span data-stu-id="d08b5-105">Returns an array of single-qubit rotations along a given axis, parameterized by distinct model parameters.</span></span>

```qsharp
function PartialRotationsLayer (idxsQubits : Int[], axis : Pauli) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a><span data-ttu-id="d08b5-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="d08b5-106">Input</span></span>

### <a name="idxsqubits--int"></a><span data-ttu-id="d08b5-107">idxsQubits: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="d08b5-107">idxsQubits : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="d08b5-108">Índices para o qubits a serem usados como os destinos para cada rotação.</span><span class="sxs-lookup"><span data-stu-id="d08b5-108">Indices for the qubits to be used as the targets for each rotation.</span></span>


### <a name="axis--pauli"></a><span data-ttu-id="d08b5-109">eixo: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="d08b5-109">axis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="d08b5-110">O eixo de rotação para cada rotação na camada especificada.</span><span class="sxs-lookup"><span data-stu-id="d08b5-110">The rotation axis for each rotation in the given layer.</span></span>



## <a name="output--controlledrotation"></a><span data-ttu-id="d08b5-111">Saída: [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="d08b5-111">Output : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="d08b5-112">Uma matriz de rotações controladas sobre o eixo determinado, uma em cada `nQubits` qubits.</span><span class="sxs-lookup"><span data-stu-id="d08b5-112">An array of controlled rotations about the given axis, one on each of `nQubits` qubits.</span></span>