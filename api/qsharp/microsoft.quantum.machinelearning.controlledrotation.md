---
uid: Microsoft.Quantum.MachineLearning.ControlledRotation
title: Tipo definido pelo usuário ControlledRotation
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ControlledRotation
qsharp.summary: Describes a controlled rotation in terms of its target and control indices, rotation axis, and index into a model parameter vector.
ms.openlocfilehash: 231afe65da3640218cbc97b9d49eae21bf6e1786
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847404"
---
# <a name="controlledrotation-user-defined-type"></a><span data-ttu-id="077b5-102">Tipo definido pelo usuário ControlledRotation</span><span class="sxs-lookup"><span data-stu-id="077b5-102">ControlledRotation user defined type</span></span>

<span data-ttu-id="077b5-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="077b5-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="077b5-104">Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="077b5-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="077b5-105">Descreve uma rotação controlada em termos de seus índices de destino e controle, eixo de rotação e índice em um vetor de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="077b5-105">Describes a controlled rotation in terms of its target and control indices, rotation axis, and index into a model parameter vector.</span></span>

```qsharp

newtype ControlledRotation = ((TargetIndex : Int, ControlIndices : Int[]), Axis : Pauli, ParameterIndex : Int);
```



## <a name="named-items"></a><span data-ttu-id="077b5-106">Itens nomeados</span><span class="sxs-lookup"><span data-stu-id="077b5-106">Named Items</span></span>

### <a name="targetindex--int"></a><span data-ttu-id="077b5-107">TargetIndex: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="077b5-107">TargetIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="077b5-108">Índice do qubit de destino para esta rotação controlada.</span><span class="sxs-lookup"><span data-stu-id="077b5-108">Index of the target qubit for this controlled rotation.</span></span>
### <a name="controlindices--int"></a><span data-ttu-id="077b5-109">ControlIndices: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="077b5-109">ControlIndices : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="077b5-110">Uma matriz dos índices de qubit de controle para essa rotação.</span><span class="sxs-lookup"><span data-stu-id="077b5-110">An array of the control qubit indices for this rotation.</span></span>
### <a name="axis--pauli"></a><span data-ttu-id="077b5-111">Eixo: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="077b5-111">Axis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="077b5-112">O eixo desta rotação.</span><span class="sxs-lookup"><span data-stu-id="077b5-112">The axis for this rotation.</span></span>
### <a name="parameterindex--int"></a><span data-ttu-id="077b5-113">ParameterIndex: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="077b5-113">ParameterIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="077b5-114">Um índice em um vetor de parâmetro de modelo que descreve o ângulo dessa rotação.</span><span class="sxs-lookup"><span data-stu-id="077b5-114">An index into a model parameter vector describing the angle for this rotation.</span></span>

## <a name="example"></a><span data-ttu-id="077b5-115">Exemplo</span><span class="sxs-lookup"><span data-stu-id="077b5-115">Example</span></span>

<span data-ttu-id="077b5-116">O seguinte representa uma rotação sobre o eixo $X $ do primeiro qubit em um registro, controlado no segundo qubit e com um ângulo fornecido pelo quarto parâmetro em um modelo sequencial:</span><span class="sxs-lookup"><span data-stu-id="077b5-116">The following represents a rotation about the $X$-axis of the first qubit in a register, controlled on the second qubit, and with an angle given by the fourth parameter in a sequential model:</span></span>

```qsharp
let controlledRotation = ControlledRotation(
    (0, [1]),
    PauliX,
    3
)
```

## <a name="remarks"></a><span data-ttu-id="077b5-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="077b5-117">Remarks</span></span>

<span data-ttu-id="077b5-118">Uma rotação não controlada pode ser representada pela configuração `ControlIndices` para uma matriz vazia de índices, `new Int[0]` .</span><span class="sxs-lookup"><span data-stu-id="077b5-118">An uncontrolled rotation can be represented by setting `ControlIndices` to an empty array of indexes, `new Int[0]`.</span></span>