---
uid: Microsoft.Quantum.Simulation.EstimateEnergyWithAdiabaticEvolution
title: Operação EstimateEnergyWithAdiabaticEvolution
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EstimateEnergyWithAdiabaticEvolution
qsharp.summary: Performs state preparation by applying a `statePrepUnitary` on an automatically allocated input state, followed by adiabatic state preparation using a `adiabaticUnitary`, and finally phase estimation with respect to `qpeUnitary`on the resulting state using a `phaseEstAlgorithm`.
ms.openlocfilehash: 3fdbdd83b784cdc560e3160151fdf4ba4e7115e6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694933"
---
# <a name="estimateenergywithadiabaticevolution-operation"></a><span data-ttu-id="a4cd5-102">Operação EstimateEnergyWithAdiabaticEvolution</span><span class="sxs-lookup"><span data-stu-id="a4cd5-102">EstimateEnergyWithAdiabaticEvolution operation</span></span>

<span data-ttu-id="a4cd5-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="a4cd5-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="a4cd5-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a4cd5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a4cd5-105">Executa a preparação do estado aplicando um `statePrepUnitary` em um estado de entrada alocado automaticamente, seguido pela preparação do estado adiabatic usando uma `adiabaticUnitary` estimativa de fase e finally com relação ao `qpeUnitary` estado resultante usando um `phaseEstAlgorithm` .</span><span class="sxs-lookup"><span data-stu-id="a4cd5-105">Performs state preparation by applying a `statePrepUnitary` on an automatically allocated input state, followed by adiabatic state preparation using a `adiabaticUnitary`, and finally phase estimation with respect to `qpeUnitary`on the resulting state using a `phaseEstAlgorithm`.</span></span>

```qsharp
operation EstimateEnergyWithAdiabaticEvolution (nQubits : Int, statePrepUnitary : (Qubit[] => Unit), adiabaticUnitary : (Qubit[] => Unit), qpeUnitary : (Qubit[] => Unit is Adj + Ctl), phaseEstAlgorithm : ((Microsoft.Quantum.Oracles.DiscreteOracle, Qubit[]) => Double)) : Double
```


## <a name="input"></a><span data-ttu-id="a4cd5-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="a4cd5-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="a4cd5-107">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a4cd5-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a4cd5-108">Número de qubits usadas para a simulação.</span><span class="sxs-lookup"><span data-stu-id="a4cd5-108">Number of qubits used for the simulation.</span></span>


### <a name="stateprepunitary--qubit--unit"></a><span data-ttu-id="a4cd5-109">statePrepUnitary: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="a4cd5-109">statePrepUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="a4cd5-110">Um Oracle representando a preparação do estado para o gerador dinâmico inicial.</span><span class="sxs-lookup"><span data-stu-id="a4cd5-110">An oracle representing state preparation for the initial dynamical generator.</span></span>


### <a name="adiabaticunitary--qubit--unit"></a><span data-ttu-id="a4cd5-111">adiabaticUnitary: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="a4cd5-111">adiabaticUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="a4cd5-112">Um Oracle que representa o algoritmo de evolução do adiabatic a ser usado para implementar as varreduras para o estado final do algoritmo.</span><span class="sxs-lookup"><span data-stu-id="a4cd5-112">An oracle representing the adiabatic evolution algorithm to be used to implement the sweeps to the final state of the algorithm.</span></span>


### <a name="qpeunitary--qubit--unit-adj--ctl"></a><span data-ttu-id="a4cd5-113">qpeUnitary: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit) do ano + CTL</span><span class="sxs-lookup"><span data-stu-id="a4cd5-113">qpeUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="a4cd5-114">Um Oracle que representa um operador unitário $U $ representando a evolução do tempo $ \delta t $ em um gerador dinâmico com estado de terra $ \ket{\phi} $ e energia de estado terrestre $E = \phi \\ , \delta t $.</span><span class="sxs-lookup"><span data-stu-id="a4cd5-114">An oracle representing a unitary operator $U$ representing evolution for time $\delta t$ under a dynamical generator with ground state $\ket{\phi}$ and ground state energy $E = \phi\\,\delta t$.</span></span>


### <a name="phaseestalgorithm--discreteoraclequbit--double"></a><span data-ttu-id="a4cd5-115">phaseEstAlgorithm: ([DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle),[qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="a4cd5-115">phaseEstAlgorithm : ([DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Double](xref:microsoft.quantum.lang-ref.double)</span></span> 

<span data-ttu-id="a4cd5-116">Uma operação que executa a estimativa de fase em uma determinada operação de unitário.</span><span class="sxs-lookup"><span data-stu-id="a4cd5-116">An operation that performs phase estimation on a given unitary operation.</span></span>
<span data-ttu-id="a4cd5-117">Consulte [estimativa de fase iterativa](/quantum/libraries/characterization#iterative-phase-estimation) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="a4cd5-117">See [iterative phase estimation](/quantum/libraries/characterization#iterative-phase-estimation) for more details.</span></span>



## <a name="output--double"></a><span data-ttu-id="a4cd5-118">Saída: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="a4cd5-118">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="a4cd5-119">Uma estimativa de $ \hat{\phi} $ do estado do solo Energy $ \phi $ do gerador representado pelo $U $.</span><span class="sxs-lookup"><span data-stu-id="a4cd5-119">An estimate $\hat{\phi}$ of the ground state energy $\phi$ of the generator represented by $U$.</span></span>