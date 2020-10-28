---
uid: Microsoft.Quantum.MachineLearning.CyclicEntanglingLayer
title: Função CyclicEntanglingLayer
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: CyclicEntanglingLayer
qsharp.summary: Returns an array of singly controlled rotations along a given axis, arranged cyclically across a register of qubits, and parameterized by distinct model parameters.
ms.openlocfilehash: 6e0f5057b35baefe2677126ba70ee4fddde7d4db
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694683"
---
# <a name="cyclicentanglinglayer-function"></a><span data-ttu-id="42ddf-102">Função CyclicEntanglingLayer</span><span class="sxs-lookup"><span data-stu-id="42ddf-102">CyclicEntanglingLayer function</span></span>

<span data-ttu-id="42ddf-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="42ddf-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="42ddf-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="42ddf-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="42ddf-105">Retorna uma matriz de rotações controladas isoladamente ao longo de um determinado eixo, organizadas de forma cíclica em um registro de qubits e parametrizadas por parâmetros de modelo distintos.</span><span class="sxs-lookup"><span data-stu-id="42ddf-105">Returns an array of singly controlled rotations along a given axis, arranged cyclically across a register of qubits, and parameterized by distinct model parameters.</span></span>

```qsharp
function CyclicEntanglingLayer (nQubits : Int, axis : Pauli, stride : Int) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a><span data-ttu-id="42ddf-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="42ddf-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="42ddf-107">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="42ddf-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="42ddf-108">O número de qubits acionadas pela camada determinada.</span><span class="sxs-lookup"><span data-stu-id="42ddf-108">The number of qubits acted on by the given layer.</span></span>


### <a name="axis--pauli"></a><span data-ttu-id="42ddf-109">eixo: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="42ddf-109">axis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="42ddf-110">O eixo de rotação para cada rotação na camada especificada.</span><span class="sxs-lookup"><span data-stu-id="42ddf-110">The rotation axis for each rotation in the given layer.</span></span>


### <a name="stride--int"></a><span data-ttu-id="42ddf-111">Stride: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="42ddf-111">stride : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="42ddf-112">A separação entre os índices de destino e de controle para cada rotação.</span><span class="sxs-lookup"><span data-stu-id="42ddf-112">The separation between the target and control indices for each rotation.</span></span>



## <a name="output--controlledrotation"></a><span data-ttu-id="42ddf-113">Saída: [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="42ddf-113">Output : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="42ddf-114">Uma matriz de rotações controladas de dois qubits, projetadas de forma cíclica em um registro de `nQubits` qubits.</span><span class="sxs-lookup"><span data-stu-id="42ddf-114">An array of two-qubit controlled rotations laid out cyclically across a register of `nQubits` qubits.</span></span>