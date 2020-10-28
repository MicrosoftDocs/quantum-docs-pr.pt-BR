---
uid: Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates
title: Operação EstimateRealOverlapBetweenStates
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateRealOverlapBetweenStates
qsharp.summary: Given two operations which each prepare copies of a state, estimates the real part of the overlap between the states prepared by each operation.
ms.openlocfilehash: 01631bcbff2bff26ddc1db4e42d90ac4f8380bd4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693837"
---
# <a name="estimaterealoverlapbetweenstates-operation"></a><span data-ttu-id="748ee-102">Operação EstimateRealOverlapBetweenStates</span><span class="sxs-lookup"><span data-stu-id="748ee-102">EstimateRealOverlapBetweenStates operation</span></span>

<span data-ttu-id="748ee-103">Namespace: [Microsoft. Quantum. caracterization](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="748ee-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="748ee-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="748ee-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="748ee-105">Considerando-se duas operações que cada uma das cópias de um estado, o estima a parte real da sobreposição entre os Estados preparados por cada operação.</span><span class="sxs-lookup"><span data-stu-id="748ee-105">Given two operations which each prepare copies of a state, estimates the real part of the overlap between the states prepared by each operation.</span></span>

```qsharp
operation EstimateRealOverlapBetweenStates (commonPreparation : (Qubit[] => Unit is Adj), preparation1 : (Qubit[] => Unit is Adj + Ctl), preparation2 : (Qubit[] => Unit is Adj + Ctl), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="748ee-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="748ee-106">Input</span></span>

### <a name="commonpreparation--qubit--unit-adj"></a><span data-ttu-id="748ee-107">commonPreparation: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => adj da [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="748ee-107">commonPreparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="748ee-108">Uma operação que prepara um estado de entrada fixo.</span><span class="sxs-lookup"><span data-stu-id="748ee-108">An operation that prepares a fixed input state.</span></span>


### <a name="preparation1--qubit--unit-adj--ctl"></a><span data-ttu-id="748ee-109">preparation1: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit) do ano + CTL</span><span class="sxs-lookup"><span data-stu-id="748ee-109">preparation1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="748ee-110">A primeira das duas operações de preparação de estado a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="748ee-110">The first of the two state preparation operations to be compared.</span></span>


### <a name="preparation2--qubit--unit-adj--ctl"></a><span data-ttu-id="748ee-111">preparation2: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit) do ano + CTL</span><span class="sxs-lookup"><span data-stu-id="748ee-111">preparation2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="748ee-112">A segunda das duas operações de preparação de estado a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="748ee-112">The second of the two state preparation operations to be compared.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="748ee-113">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="748ee-113">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="748ee-114">O número de qubits em que `commonPreparation` , `preparation1` e `preparation2` todos os Act.</span><span class="sxs-lookup"><span data-stu-id="748ee-114">The number of qubits on which `commonPreparation`, `preparation1`, and `preparation2` all act.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="748ee-115">nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="748ee-115">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="748ee-116">O número de medições a serem usadas para estimar a sobreposição.</span><span class="sxs-lookup"><span data-stu-id="748ee-116">The number of measurements to use in estimating the overlap.</span></span>



## <a name="output--double"></a><span data-ttu-id="748ee-117">Saída: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="748ee-117">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="748ee-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="748ee-118">Remarks</span></span>

<span data-ttu-id="748ee-119">Esta operação usa o teste Hadamard para encontrar a parte real de $ $ \begin{align} \braket{\psi | V ^ {\dagger} U | \psi} \end{Align} $ $, em que $ \ket{\psi} $ é o estado preparado pelo `commonPreparation` , $U $ é a representação unitário da ação de `preparation1` e onde $V $ corresponde a `preparation2` .</span><span class="sxs-lookup"><span data-stu-id="748ee-119">This operation uses the Hadamard test to find the real part of $$ \begin{align} \braket{\psi | V^{\dagger} U | \psi} \end{align} $$ where $\ket{\psi}$ is the state prepared by `commonPreparation`, $U$ is the unitary representation of the action of `preparation1`, and where $V$ corresponds to `preparation2`.</span></span>

## <a name="references"></a><span data-ttu-id="748ee-120">Referências</span><span class="sxs-lookup"><span data-stu-id="748ee-120">References</span></span>

- <span data-ttu-id="748ee-121">Aharonov *et al.* [Quant-pH/0511096](https://arxiv.org/abs/quant-ph/0511096).</span><span class="sxs-lookup"><span data-stu-id="748ee-121">Aharonov *et al.* [quant-ph/0511096](https://arxiv.org/abs/quant-ph/0511096).</span></span>

## <a name="see-also"></a><span data-ttu-id="748ee-122">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="748ee-122">See Also</span></span>

- [<span data-ttu-id="748ee-123">Microsoft. Quantum. Caracterization. EstimateImagOverlapBetweenStates</span><span class="sxs-lookup"><span data-stu-id="748ee-123">Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates</span></span>](xref:Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates)
- [<span data-ttu-id="748ee-124">Microsoft. Quantum. Caracterization. EstimateOverlapBetweenStates</span><span class="sxs-lookup"><span data-stu-id="748ee-124">Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates</span></span>](xref:Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates)