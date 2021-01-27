---
uid: Microsoft.Quantum.Simulation.InterpolatedEvolution
title: Função InterpolatedEvolution
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: InterpolatedEvolution
qsharp.summary: Interpolates between two generators with a uniform schedule, returning an operation that applies simulated evolution under the resulting time-dependent generator to a qubit register.
ms.openlocfilehash: 4d2e04513c96c6e5f41e85f1df685e91e2973098
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858083"
---
# <a name="interpolatedevolution-function"></a><span data-ttu-id="838f9-102">Função InterpolatedEvolution</span><span class="sxs-lookup"><span data-stu-id="838f9-102">InterpolatedEvolution function</span></span>

<span data-ttu-id="838f9-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="838f9-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="838f9-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="838f9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="838f9-105">Interpola entre dois geradores com um agendamento uniforme, retornando uma operação que aplica a evolução simulada sob o gerador dependente de tempo resultante a um registro de qubit.</span><span class="sxs-lookup"><span data-stu-id="838f9-105">Interpolates between two generators with a uniform schedule, returning an operation that applies simulated evolution under the resulting time-dependent generator to a qubit register.</span></span>

```qsharp
function InterpolatedEvolution (interpolationTime : Double, evolutionGeneratorStart : Microsoft.Quantum.Simulation.EvolutionGenerator, evolutionGeneratorEnd : Microsoft.Quantum.Simulation.EvolutionGenerator, timeDependentSimulationAlgorithm : Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="838f9-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="838f9-106">Input</span></span>

### <a name="interpolationtime--double"></a><span data-ttu-id="838f9-107">interpolação: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="838f9-107">interpolationTime : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="838f9-108">Tempo para realizar a interpolação.</span><span class="sxs-lookup"><span data-stu-id="838f9-108">Time to perform the interpolation over.</span></span>


### <a name="evolutiongeneratorstart--evolutiongenerator"></a><span data-ttu-id="838f9-109">evolutionGeneratorStart: [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span><span class="sxs-lookup"><span data-stu-id="838f9-109">evolutionGeneratorStart : [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span></span>

<span data-ttu-id="838f9-110">Gerador inicial para simular a evolução.</span><span class="sxs-lookup"><span data-stu-id="838f9-110">Initial generator to simulate evolution under.</span></span>


### <a name="evolutiongeneratorend--evolutiongenerator"></a><span data-ttu-id="838f9-111">evolutionGeneratorEnd: [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span><span class="sxs-lookup"><span data-stu-id="838f9-111">evolutionGeneratorEnd : [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span></span>

<span data-ttu-id="838f9-112">O gerador final para simular a evolução.</span><span class="sxs-lookup"><span data-stu-id="838f9-112">Final generator to simulate evolution under.</span></span>


### <a name="timedependentsimulationalgorithm--timedependentsimulationalgorithm"></a><span data-ttu-id="838f9-113">timeDependentSimulationAlgorithm: [timeDependentSimulationAlgorithm](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)</span><span class="sxs-lookup"><span data-stu-id="838f9-113">timeDependentSimulationAlgorithm : [TimeDependentSimulationAlgorithm](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)</span></span>

<span data-ttu-id="838f9-114">Um algoritmo de simulação dependente de tempo que será usado para simular a evolução durante o agendamento de interpolação uniforme.</span><span class="sxs-lookup"><span data-stu-id="838f9-114">A time-dependent simulation algorithm that will be used to simulate evolution during the uniform interpolation schedule.</span></span>



## <a name="output--qubit--unit--is-adj--ctl"></a><span data-ttu-id="838f9-115">Saída: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="838f9-115">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>



## <a name="remarks"></a><span data-ttu-id="838f9-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="838f9-116">Remarks</span></span>

<span data-ttu-id="838f9-117">Se o tempo de interpolação for escolhido para atender às condições adiabatic, essa função retornará uma operação que executa a preparação do estado adiabatic para o gerador dinâmico final.</span><span class="sxs-lookup"><span data-stu-id="838f9-117">If the interpolation time is chosen to meet the adiabatic conditions, then this function returns an operation which performs adiabatic state preparation for the final dynamical generator.</span></span>