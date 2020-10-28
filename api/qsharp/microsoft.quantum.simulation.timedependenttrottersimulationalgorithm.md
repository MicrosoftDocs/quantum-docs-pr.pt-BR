---
uid: Microsoft.Quantum.Simulation.TimeDependentTrotterSimulationAlgorithm
title: Função TimeDependentTrotterSimulationAlgorithm
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentTrotterSimulationAlgorithm
qsharp.summary: '`TimeDependentSimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate a unitary operator that solves the time-dependent Schrodinger equation.'
ms.openlocfilehash: 6129d768276b5c9d96a1b1ed9cd5a6a22d28e286
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694576"
---
# <a name="timedependenttrottersimulationalgorithm-function"></a><span data-ttu-id="ca05a-102">Função TimeDependentTrotterSimulationAlgorithm</span><span class="sxs-lookup"><span data-stu-id="ca05a-102">TimeDependentTrotterSimulationAlgorithm function</span></span>

<span data-ttu-id="ca05a-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="ca05a-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="ca05a-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ca05a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ca05a-105">`TimeDependentSimulationAlgorithm` função que usa uma decomposição Trotter – Suzuki para aproximar um operador unitário que resolve a equação de Schrodinger dependente de tempo.</span><span class="sxs-lookup"><span data-stu-id="ca05a-105">`TimeDependentSimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate a unitary operator that solves the time-dependent Schrodinger equation.</span></span>

```qsharp
function TimeDependentTrotterSimulationAlgorithm (trotterStepSize : Double, trotterOrder : Int) : Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm
```


## <a name="input"></a><span data-ttu-id="ca05a-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="ca05a-106">Input</span></span>

### <a name="trotterstepsize--double"></a><span data-ttu-id="ca05a-107">trotterStepSize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ca05a-107">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ca05a-108">Duração da evolução de tempo simulada em uma única etapa de Trotter.</span><span class="sxs-lookup"><span data-stu-id="ca05a-108">Duration of simulated time-evolution in single Trotter step.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="ca05a-109">trotterOrder: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ca05a-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ca05a-110">Ordem do integrador Trotter.</span><span class="sxs-lookup"><span data-stu-id="ca05a-110">Order of Trotter integrator.</span></span> <span data-ttu-id="ca05a-111">Deve ser 1 ou um número par.</span><span class="sxs-lookup"><span data-stu-id="ca05a-111">This must be either 1 or an even number.</span></span>



## <a name="output--timedependentsimulationalgorithm"></a><span data-ttu-id="ca05a-112">Saída: [TimeDependentSimulationAlgorithm](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)</span><span class="sxs-lookup"><span data-stu-id="ca05a-112">Output : [TimeDependentSimulationAlgorithm](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)</span></span>

<span data-ttu-id="ca05a-113">Um tipo `TimeDependentSimulationAlgorithm`.</span><span class="sxs-lookup"><span data-stu-id="ca05a-113">A `TimeDependentSimulationAlgorithm` type.</span></span>