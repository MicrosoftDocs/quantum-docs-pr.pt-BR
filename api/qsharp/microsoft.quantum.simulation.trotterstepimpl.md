---
uid: Microsoft.Quantum.Simulation.TrotterStepImpl
title: Operação TrotterStepImpl
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterStepImpl
qsharp.summary: Implements time-evolution by a term contained in a `GeneratorSystem`.
ms.openlocfilehash: 1ddd7ab33df243d729b5b48cba393d976bfd3640
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92697069"
---
# <a name="trotterstepimpl-operation"></a><span data-ttu-id="f4fde-102">Operação TrotterStepImpl</span><span class="sxs-lookup"><span data-stu-id="f4fde-102">TrotterStepImpl operation</span></span>

<span data-ttu-id="f4fde-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="f4fde-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="f4fde-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f4fde-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f4fde-105">Implementa a evolução de tempo por um termo contido em um `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="f4fde-105">Implements time-evolution by a term contained in a `GeneratorSystem`.</span></span>

```qsharp
operation TrotterStepImpl (evolutionGenerator : Microsoft.Quantum.Simulation.EvolutionGenerator, idx : Int, stepsize : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="f4fde-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="f4fde-106">Input</span></span>

### <a name="evolutiongenerator--evolutiongenerator"></a><span data-ttu-id="f4fde-107">evolutionGenerator: [evolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span><span class="sxs-lookup"><span data-stu-id="f4fde-107">evolutionGenerator : [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span></span>

<span data-ttu-id="f4fde-108">Uma descrição completa do sistema a ser simulado.</span><span class="sxs-lookup"><span data-stu-id="f4fde-108">A complete description of the system to be simulated.</span></span>


### <a name="idx--int"></a><span data-ttu-id="f4fde-109">IDX: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f4fde-109">idx : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f4fde-110">Índice de inteiro para um termo no sistema descrito.</span><span class="sxs-lookup"><span data-stu-id="f4fde-110">Integer index to a term in the described system.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="f4fde-111">etapas: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f4fde-111">stepsize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f4fde-112">Multiplicador na duração da evolução do tempo por termo indexado por `idx` .</span><span class="sxs-lookup"><span data-stu-id="f4fde-112">Multiplier on duration of time-evolution by term indexed by `idx`.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="f4fde-113">qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="f4fde-113">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="f4fde-114">Qubits atuou por simulação.</span><span class="sxs-lookup"><span data-stu-id="f4fde-114">Qubits acted on by simulation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f4fde-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f4fde-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

