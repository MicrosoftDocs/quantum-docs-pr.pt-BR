---
uid: Microsoft.Quantum.MachineLearning.ControlledRotation
title: Tipo definido pelo usuário ControlledRotation
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ControlledRotation
qsharp.summary: Describes a controlled rotation in terms of its target and control indices, rotation axis, and index into a model parameter vector.
ms.openlocfilehash: afc425c16ab550fd414e656484c9ff6f0f8f3ef4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693321"
---
# <a name="controlledrotation-user-defined-type"></a><span data-ttu-id="3765b-102">Tipo definido pelo usuário ControlledRotation</span><span class="sxs-lookup"><span data-stu-id="3765b-102">ControlledRotation user defined type</span></span>

<span data-ttu-id="3765b-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="3765b-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="3765b-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3765b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3765b-105">Descreve uma rotação controlada em termos de seus índices de destino e controle, eixo de rotação e índice em um vetor de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="3765b-105">Describes a controlled rotation in terms of its target and control indices, rotation axis, and index into a model parameter vector.</span></span>

```qsharp

newtype ControlledRotation = ((TargetIndex : Int, ControlIndices : Int[]), Axis : Pauli, ParameterIndex : Int);
```



## <a name="named-items"></a><span data-ttu-id="3765b-106">Itens nomeados</span><span class="sxs-lookup"><span data-stu-id="3765b-106">Named Items</span></span>

### <a name="targetindex--int"></a><span data-ttu-id="3765b-107">TargetIndex: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3765b-107">TargetIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3765b-108">Índice do qubit de destino para esta rotação controlada.</span><span class="sxs-lookup"><span data-stu-id="3765b-108">Index of the target qubit for this controlled rotation.</span></span>
### <a name="controlindices--int"></a><span data-ttu-id="3765b-109">ControlIndices: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="3765b-109">ControlIndices : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="3765b-110">Uma matriz dos índices de qubit de controle para essa rotação.</span><span class="sxs-lookup"><span data-stu-id="3765b-110">An array of the control qubit indices for this rotation.</span></span>
### <a name="axis--pauli"></a><span data-ttu-id="3765b-111">Eixo: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="3765b-111">Axis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="3765b-112">O eixo desta rotação.</span><span class="sxs-lookup"><span data-stu-id="3765b-112">The axis for this rotation.</span></span>
### <a name="parameterindex--int"></a><span data-ttu-id="3765b-113">ParameterIndex: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3765b-113">ParameterIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3765b-114">Um índice em um vetor de parâmetro de modelo que descreve o ângulo dessa rotação.</span><span class="sxs-lookup"><span data-stu-id="3765b-114">An index into a model parameter vector describing the angle for this rotation.</span></span>

## <a name="remarks"></a><span data-ttu-id="3765b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="3765b-115">Remarks</span></span>

<span data-ttu-id="3765b-116">Uma rotação não controlada pode ser representada pela configuração `ControlIndices` para uma matriz vazia de índices, `new Int[0]` .</span><span class="sxs-lookup"><span data-stu-id="3765b-116">An uncontrolled rotation can be represented by setting `ControlIndices` to an empty array of indexes, `new Int[0]`.</span></span>