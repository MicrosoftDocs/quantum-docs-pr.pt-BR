---
uid: Microsoft.Quantum.Simulation.TrotterSimulationAlgorithm
title: Função TrotterSimulationAlgorithm
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterSimulationAlgorithm
qsharp.summary: '`SimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate the time-evolution operator _exp(-iHt)_.'
ms.openlocfilehash: c52acf293e69c78e7a82b0cf5d94de52d0f5a293
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694575"
---
# <a name="trottersimulationalgorithm-function"></a><span data-ttu-id="4c30f-102">Função TrotterSimulationAlgorithm</span><span class="sxs-lookup"><span data-stu-id="4c30f-102">TrotterSimulationAlgorithm function</span></span>

<span data-ttu-id="4c30f-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="4c30f-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="4c30f-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4c30f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4c30f-105">`SimulationAlgorithm` função que usa uma decomposição Trotter – Suzuki para aproximar o operador de tempo-evolução _exp (-IHT)_ .</span><span class="sxs-lookup"><span data-stu-id="4c30f-105">`SimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate the time-evolution operator _exp(-iHt)_ .</span></span>

```qsharp
function TrotterSimulationAlgorithm (trotterStepSize : Double, trotterOrder : Int) : Microsoft.Quantum.Simulation.SimulationAlgorithm
```


## <a name="input"></a><span data-ttu-id="4c30f-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="4c30f-106">Input</span></span>

### <a name="trotterstepsize--double"></a><span data-ttu-id="4c30f-107">trotterStepSize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="4c30f-107">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="4c30f-108">Duração da evolução de tempo simulada em uma única etapa de Trotter.</span><span class="sxs-lookup"><span data-stu-id="4c30f-108">Duration of simulated time-evolution in single Trotter step.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="4c30f-109">trotterOrder: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4c30f-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4c30f-110">Ordem do integrador Trotter.</span><span class="sxs-lookup"><span data-stu-id="4c30f-110">Order of Trotter integrator.</span></span> <span data-ttu-id="4c30f-111">Deve ser 1 ou um número par.</span><span class="sxs-lookup"><span data-stu-id="4c30f-111">This must be either 1 or an even number.</span></span>



## <a name="output--simulationalgorithm"></a><span data-ttu-id="4c30f-112">Saída: [SimulationAlgorithm](xref:Microsoft.Quantum.Simulation.SimulationAlgorithm)</span><span class="sxs-lookup"><span data-stu-id="4c30f-112">Output : [SimulationAlgorithm](xref:Microsoft.Quantum.Simulation.SimulationAlgorithm)</span></span>

<span data-ttu-id="4c30f-113">Um tipo `SimulationAlgorithm`.</span><span class="sxs-lookup"><span data-stu-id="4c30f-113">A `SimulationAlgorithm` type.</span></span>