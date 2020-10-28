---
uid: Microsoft.Quantum.Simulation.TrotterSimulationAlgorithmImpl
title: Operação TrotterSimulationAlgorithmImpl
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterSimulationAlgorithmImpl
qsharp.summary: Makes repeated calls to `TrotterStep` to approximate the time-evolution operator exp(_-iHt_).
ms.openlocfilehash: 2af68532d700a1fb5b037707ce4650696cbe1a64
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92697074"
---
# <a name="trottersimulationalgorithmimpl-operation"></a><span data-ttu-id="86c8d-102">Operação TrotterSimulationAlgorithmImpl</span><span class="sxs-lookup"><span data-stu-id="86c8d-102">TrotterSimulationAlgorithmImpl operation</span></span>

<span data-ttu-id="86c8d-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="86c8d-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="86c8d-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="86c8d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="86c8d-105">Faz chamadas repetidas para `TrotterStep` para aproximar o operador de tempo de evolução exp ( _-IHT_ ).</span><span class="sxs-lookup"><span data-stu-id="86c8d-105">Makes repeated calls to `TrotterStep` to approximate the time-evolution operator exp( _-iHt_ ).</span></span>

```qsharp
operation TrotterSimulationAlgorithmImpl (trotterStepSize : Double, trotterOrder : Int, maxTime : Double, evolutionGenerator : Microsoft.Quantum.Simulation.EvolutionGenerator, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="86c8d-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="86c8d-106">Input</span></span>

### <a name="trotterstepsize--double"></a><span data-ttu-id="86c8d-107">trotterStepSize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="86c8d-107">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="86c8d-108">Duração da evolução de tempo simulada em uma única etapa de Trotter.</span><span class="sxs-lookup"><span data-stu-id="86c8d-108">Duration of simulated time-evolution in single Trotter step.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="86c8d-109">trotterOrder: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="86c8d-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="86c8d-110">Ordem do integrador Trotter.</span><span class="sxs-lookup"><span data-stu-id="86c8d-110">Order of Trotter integrator.</span></span> <span data-ttu-id="86c8d-111">Deve ser 1 ou um número par.</span><span class="sxs-lookup"><span data-stu-id="86c8d-111">This must be either 1 or an even number.</span></span>


### <a name="maxtime--double"></a><span data-ttu-id="86c8d-112">maxTime: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="86c8d-112">maxTime : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="86c8d-113">Duração total da simulação $t $.</span><span class="sxs-lookup"><span data-stu-id="86c8d-113">Total duration of simulation $t$.</span></span>


### <a name="evolutiongenerator--evolutiongenerator"></a><span data-ttu-id="86c8d-114">evolutionGenerator: [evolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span><span class="sxs-lookup"><span data-stu-id="86c8d-114">evolutionGenerator : [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span></span>

<span data-ttu-id="86c8d-115">Uma descrição completa do sistema a ser simulado.</span><span class="sxs-lookup"><span data-stu-id="86c8d-115">A complete description of the system to be simulated.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="86c8d-116">qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="86c8d-116">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="86c8d-117">Qubits atuou por simulação.</span><span class="sxs-lookup"><span data-stu-id="86c8d-117">Qubits acted on by simulation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="86c8d-118">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="86c8d-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

