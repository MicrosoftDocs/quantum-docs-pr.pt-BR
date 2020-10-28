---
uid: Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates
title: Operação EstimateOverlapBetweenStates
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateOverlapBetweenStates
qsharp.summary: Given two operations which each prepare copies of a state, estimates the squared overlap between the states prepared by each operation.
ms.openlocfilehash: 58a367c7ff7d13ac5c1eb1588fb8dac66414776c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693840"
---
# <a name="estimateoverlapbetweenstates-operation"></a><span data-ttu-id="4a491-102">Operação EstimateOverlapBetweenStates</span><span class="sxs-lookup"><span data-stu-id="4a491-102">EstimateOverlapBetweenStates operation</span></span>

<span data-ttu-id="4a491-103">Namespace: [Microsoft. Quantum. caracterization](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="4a491-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="4a491-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4a491-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4a491-105">Dadas duas operações que cada uma das cópias de um estado, o estima a sobreposição de quadrado entre os Estados preparados por cada operação.</span><span class="sxs-lookup"><span data-stu-id="4a491-105">Given two operations which each prepare copies of a state, estimates the squared overlap between the states prepared by each operation.</span></span>

```qsharp
operation EstimateOverlapBetweenStates (preparation1 : (Qubit[] => Unit is Adj), preparation2 : (Qubit[] => Unit is Adj), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="4a491-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="4a491-106">Input</span></span>

### <a name="preparation1--qubit--unit-adj"></a><span data-ttu-id="4a491-107">preparation1: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => adj da [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4a491-107">preparation1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="4a491-108">A primeira das duas operações de preparação de estado a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="4a491-108">The first of the two state preparation operations to be compared.</span></span>


### <a name="preparation2--qubit--unit-adj"></a><span data-ttu-id="4a491-109">preparation2: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => adj da [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4a491-109">preparation2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="4a491-110">A segunda das duas operações de preparação de estado a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="4a491-110">The second of the two state preparation operations to be compared.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="4a491-111">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4a491-111">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4a491-112">O número de qubits em que `commonPreparation` , `preparation1` e `preparation2` todos os Act.</span><span class="sxs-lookup"><span data-stu-id="4a491-112">The number of qubits on which `commonPreparation`, `preparation1`, and `preparation2` all act.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="4a491-113">nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4a491-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4a491-114">O número de medições a serem usadas para estimar a sobreposição.</span><span class="sxs-lookup"><span data-stu-id="4a491-114">The number of measurements to use in estimating the overlap.</span></span>



## <a name="output--double"></a><span data-ttu-id="4a491-115">Saída: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="4a491-115">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="4a491-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a491-116">Remarks</span></span>

<span data-ttu-id="4a491-117">Esta operação usa o teste de permuta para localizar $ $ \begin{align} \left | \braket{00\cdots 0 | V ^ {\dagger} U | 00 \ cdots 0} \right | ^ 2 \end{Align} $ $, em que $U $ é a representação unitário da ação de `preparation1` e onde $V $ corresponde a `preparation2` .</span><span class="sxs-lookup"><span data-stu-id="4a491-117">This operation uses the SWAP test to find $$ \begin{align} \left| \braket{00\cdots 0 | V^{\dagger} U | 00\cdots 0} \right|^2 \end{align} $$ where $U$ is the unitary representation of the action of `preparation1`, and where $V$ corresponds to `preparation2`.</span></span>

## <a name="see-also"></a><span data-ttu-id="4a491-118">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="4a491-118">See Also</span></span>

- [<span data-ttu-id="4a491-119">Microsoft. Quantum. Caracterization. EstimateRealOverlapBetweenStates</span><span class="sxs-lookup"><span data-stu-id="4a491-119">Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates</span></span>](xref:Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates)
- [<span data-ttu-id="4a491-120">Microsoft. Quantum. Caracterization. EstimateImagOverlapBetweenStates</span><span class="sxs-lookup"><span data-stu-id="4a491-120">Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates</span></span>](xref:Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates)