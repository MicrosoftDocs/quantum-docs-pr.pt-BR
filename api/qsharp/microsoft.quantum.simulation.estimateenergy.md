---
uid: Microsoft.Quantum.Simulation.EstimateEnergy
title: Operação EstimateEnergy
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EstimateEnergy
qsharp.summary: Performs state preparation by applying a `statePrepUnitary` on an automatically allocated input state phase estimation with respect to `qpeUnitary`on the resulting state using a `phaseEstAlgorithm`.
ms.openlocfilehash: 0a02a8aad891c45b184b9b18d4e9383236485940
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229487"
---
# <a name="estimateenergy-operation"></a><span data-ttu-id="bf98c-102">Operação EstimateEnergy</span><span class="sxs-lookup"><span data-stu-id="bf98c-102">EstimateEnergy operation</span></span>

<span data-ttu-id="bf98c-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="bf98c-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="bf98c-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bf98c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bf98c-105">Executa a preparação do estado aplicando um `statePrepUnitary` em uma estimativa de fase de estado de entrada alocada automaticamente em relação ao `qpeUnitary` estado resultante usando um `phaseEstAlgorithm` .</span><span class="sxs-lookup"><span data-stu-id="bf98c-105">Performs state preparation by applying a `statePrepUnitary` on an automatically allocated input state phase estimation with respect to `qpeUnitary`on the resulting state using a `phaseEstAlgorithm`.</span></span>

```qsharp
operation EstimateEnergy (nQubits : Int, statePrepUnitary : (Qubit[] => Unit), qpeUnitary : (Qubit[] => Unit is Adj + Ctl), phaseEstAlgorithm : ((Microsoft.Quantum.Oracles.DiscreteOracle, Qubit[]) => Double)) : Double
```


## <a name="input"></a><span data-ttu-id="bf98c-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="bf98c-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="bf98c-107">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bf98c-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bf98c-108">Número de qubits usadas para executar a simulação.</span><span class="sxs-lookup"><span data-stu-id="bf98c-108">Number of qubits used to perform simulation.</span></span>


### <a name="stateprepunitary--qubit--unit"></a><span data-ttu-id="bf98c-109">statePrepUnitary: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="bf98c-109">statePrepUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="bf98c-110">Um Oracle representando a preparação do estado para o gerador dinâmico inicial.</span><span class="sxs-lookup"><span data-stu-id="bf98c-110">An oracle representing state preparation for the initial dynamical generator.</span></span>


### <a name="qpeunitary--qubit--unit--is-adj--ctl"></a><span data-ttu-id="bf98c-111">qpeUnitary: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="bf98c-111">qpeUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="bf98c-112">Um Oracle que representa um operador unitário $U $ representando a evolução do tempo $ \delta t $ em um gerador dinâmico com estado de terra $ \ket{\phi} $ e energia de estado terrestre $E = \phi \\ , \delta t $.</span><span class="sxs-lookup"><span data-stu-id="bf98c-112">An oracle representing a unitary operator $U$ representing evolution for time $\delta t$ under a dynamical generator with ground state $\ket{\phi}$ and ground state energy $E = \phi\\,\delta t$.</span></span>


### <a name="phaseestalgorithm--discreteoraclequbit--double"></a><span data-ttu-id="bf98c-113">phaseEstAlgorithm: ([DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle),[qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="bf98c-113">phaseEstAlgorithm : ([DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Double](xref:microsoft.quantum.lang-ref.double)</span></span> 

<span data-ttu-id="bf98c-114">Uma operação que executa a estimativa de fase em uma determinada operação de unitário.</span><span class="sxs-lookup"><span data-stu-id="bf98c-114">An operation that performs phase estimation on a given unitary operation.</span></span>
<span data-ttu-id="bf98c-115">Consulte [estimativa de fase iterativa](/quantum/libraries/characterization#iterative-phase-estimation) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="bf98c-115">See [iterative phase estimation](/quantum/libraries/characterization#iterative-phase-estimation) for more details.</span></span>



## <a name="output--double"></a><span data-ttu-id="bf98c-116">Saída: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="bf98c-116">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="bf98c-117">Uma estimativa de $ \hat{\phi} $ do estado do solo Energy $ \phi $ da energia de estado terrestre do gerador representado pelo $U $.</span><span class="sxs-lookup"><span data-stu-id="bf98c-117">An estimate $\hat{\phi}$ of the ground state energy $\phi$ of the ground state energy of the generator represented by $U$.</span></span>