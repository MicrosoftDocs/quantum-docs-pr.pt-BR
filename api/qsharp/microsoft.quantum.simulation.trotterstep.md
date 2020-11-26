---
uid: Microsoft.Quantum.Simulation.TrotterStep
title: Função TrotterStep
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterStep
qsharp.summary: Implements a single time-step of time-evolution by the system described in an `EvolutionGenerator` using a Trotter–Suzuki decomposition.
ms.openlocfilehash: 516b40ac9920a4a8acc09ad7f558db88dbeb41e8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192801"
---
# <a name="trotterstep-function"></a><span data-ttu-id="8e3c0-102">Função TrotterStep</span><span class="sxs-lookup"><span data-stu-id="8e3c0-102">TrotterStep function</span></span>

<span data-ttu-id="8e3c0-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="8e3c0-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="8e3c0-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8e3c0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8e3c0-105">Implementa uma única etapa de tempo de evolução de tempo pelo sistema descrito em um `EvolutionGenerator` usando uma decomposição Trotter – Suzuki.</span><span class="sxs-lookup"><span data-stu-id="8e3c0-105">Implements a single time-step of time-evolution by the system described in an `EvolutionGenerator` using a Trotter–Suzuki decomposition.</span></span>

```qsharp
function TrotterStep (evolutionGenerator : Microsoft.Quantum.Simulation.EvolutionGenerator, trotterOrder : Int, trotterStepSize : Double) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="8e3c0-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="8e3c0-106">Input</span></span>

### <a name="evolutiongenerator--evolutiongenerator"></a><span data-ttu-id="8e3c0-107">evolutionGenerator: [evolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span><span class="sxs-lookup"><span data-stu-id="8e3c0-107">evolutionGenerator : [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span></span>

<span data-ttu-id="8e3c0-108">Uma descrição completa do sistema a ser simulado.</span><span class="sxs-lookup"><span data-stu-id="8e3c0-108">A complete description of the system to be simulated.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="8e3c0-109">trotterOrder: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8e3c0-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8e3c0-110">Ordem do integrador Trotter.</span><span class="sxs-lookup"><span data-stu-id="8e3c0-110">Order of Trotter integrator.</span></span> <span data-ttu-id="8e3c0-111">Deve ser 1 ou um número par.</span><span class="sxs-lookup"><span data-stu-id="8e3c0-111">This must be either 1 or an even number.</span></span>


### <a name="trotterstepsize--double"></a><span data-ttu-id="8e3c0-112">trotterStepSize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8e3c0-112">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8e3c0-113">Duração da evolução de tempo simulada em uma única etapa de Trotter.</span><span class="sxs-lookup"><span data-stu-id="8e3c0-113">Duration of simulated time-evolution in single Trotter step.</span></span>



## <a name="output--qubit--unit--is-adj--ctl"></a><span data-ttu-id="8e3c0-114">Saída: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="8e3c0-114">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="8e3c0-115">Operação unitário que aproxima uma única etapa da evolução do tempo para duração `trotterStepSize` .</span><span class="sxs-lookup"><span data-stu-id="8e3c0-115">Unitary operation that approximates a single step of time-evolution for duration `trotterStepSize`.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e3c0-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e3c0-116">Remarks</span></span>

<span data-ttu-id="8e3c0-117">Para obter mais informações sobre a decomposição Trotter – Suzuki, consulte [composição de tempo ordenado](/quantum/libraries/control-flow#time-ordered-composition).</span><span class="sxs-lookup"><span data-stu-id="8e3c0-117">For more on the Trotter–Suzuki decomposition, see [Time-Ordered Composition](/quantum/libraries/control-flow#time-ordered-composition).</span></span>