---
uid: Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates
title: Operação EstimateRealOverlapBetweenStates
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateRealOverlapBetweenStates
qsharp.summary: Given two operations which each prepare copies of a state, estimates the real part of the overlap between the states prepared by each operation.
ms.openlocfilehash: d9f569ceffc16f377189dc94035213b9075609cc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216176"
---
# <a name="estimaterealoverlapbetweenstates-operation"></a><span data-ttu-id="14168-102">Operação EstimateRealOverlapBetweenStates</span><span class="sxs-lookup"><span data-stu-id="14168-102">EstimateRealOverlapBetweenStates operation</span></span>

<span data-ttu-id="14168-103">Namespace: [Microsoft. Quantum. caracterization](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="14168-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="14168-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="14168-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="14168-105">Considerando-se duas operações que cada uma das cópias de um estado, o estima a parte real da sobreposição entre os Estados preparados por cada operação.</span><span class="sxs-lookup"><span data-stu-id="14168-105">Given two operations which each prepare copies of a state, estimates the real part of the overlap between the states prepared by each operation.</span></span>

```qsharp
operation EstimateRealOverlapBetweenStates (commonPreparation : (Qubit[] => Unit is Adj), preparation1 : (Qubit[] => Unit is Adj + Ctl), preparation2 : (Qubit[] => Unit is Adj + Ctl), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="14168-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="14168-106">Input</span></span>

### <a name="commonpreparation--qubit--unit--is-adj"></a><span data-ttu-id="14168-107">commonPreparation: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj</span><span class="sxs-lookup"><span data-stu-id="14168-107">commonPreparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="14168-108">Uma operação que prepara um estado de entrada fixo.</span><span class="sxs-lookup"><span data-stu-id="14168-108">An operation that prepares a fixed input state.</span></span>


### <a name="preparation1--qubit--unit--is-adj--ctl"></a><span data-ttu-id="14168-109">preparation1: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="14168-109">preparation1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="14168-110">A primeira das duas operações de preparação de estado a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="14168-110">The first of the two state preparation operations to be compared.</span></span>


### <a name="preparation2--qubit--unit--is-adj--ctl"></a><span data-ttu-id="14168-111">preparation2: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="14168-111">preparation2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="14168-112">A segunda das duas operações de preparação de estado a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="14168-112">The second of the two state preparation operations to be compared.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="14168-113">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="14168-113">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="14168-114">O número de qubits em que `commonPreparation` , `preparation1` e `preparation2` todos os Act.</span><span class="sxs-lookup"><span data-stu-id="14168-114">The number of qubits on which `commonPreparation`, `preparation1`, and `preparation2` all act.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="14168-115">nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="14168-115">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="14168-116">O número de medições a serem usadas para estimar a sobreposição.</span><span class="sxs-lookup"><span data-stu-id="14168-116">The number of measurements to use in estimating the overlap.</span></span>



## <a name="output--double"></a><span data-ttu-id="14168-117">Saída: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="14168-117">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="14168-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="14168-118">Remarks</span></span>

<span data-ttu-id="14168-119">Esta operação usa o teste Hadamard para encontrar a parte real de $ $ \begin{align} \braket{\psi | V ^ {\dagger} U | \psi} \end{Align} $ $, em que $ \ket{\psi} $ é o estado preparado pelo `commonPreparation` , $U $ é a representação unitário da ação de `preparation1` e onde $V $ corresponde a `preparation2` .</span><span class="sxs-lookup"><span data-stu-id="14168-119">This operation uses the Hadamard test to find the real part of $$ \begin{align} \braket{\psi | V^{\dagger} U | \psi} \end{align} $$ where $\ket{\psi}$ is the state prepared by `commonPreparation`, $U$ is the unitary representation of the action of `preparation1`, and where $V$ corresponds to `preparation2`.</span></span>

## <a name="references"></a><span data-ttu-id="14168-120">Referências</span><span class="sxs-lookup"><span data-stu-id="14168-120">References</span></span>

- <span data-ttu-id="14168-121">Aharonov *et al.* [Quant-pH/0511096](https://arxiv.org/abs/quant-ph/0511096).</span><span class="sxs-lookup"><span data-stu-id="14168-121">Aharonov *et al.* [quant-ph/0511096](https://arxiv.org/abs/quant-ph/0511096).</span></span>

## <a name="see-also"></a><span data-ttu-id="14168-122">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="14168-122">See Also</span></span>

- [<span data-ttu-id="14168-123">Microsoft. Quantum. Caracterization. EstimateImagOverlapBetweenStates</span><span class="sxs-lookup"><span data-stu-id="14168-123">Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates</span></span>](xref:Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates)
- [<span data-ttu-id="14168-124">Microsoft. Quantum. Caracterization. EstimateOverlapBetweenStates</span><span class="sxs-lookup"><span data-stu-id="14168-124">Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates</span></span>](xref:Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates)