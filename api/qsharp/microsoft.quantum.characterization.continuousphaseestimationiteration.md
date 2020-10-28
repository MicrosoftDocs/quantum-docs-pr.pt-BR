---
uid: Microsoft.Quantum.Characterization.ContinuousPhaseEstimationIteration
title: Operação ContinuousPhaseEstimationIteration
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: ContinuousPhaseEstimationIteration
qsharp.summary: Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using arbitrary real powers of a unitary oracle.
ms.openlocfilehash: a3914a4b19e3b898b6de8808699da09d386f487a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693852"
---
# <a name="continuousphaseestimationiteration-operation"></a><span data-ttu-id="f4573-102">Operação ContinuousPhaseEstimationIteration</span><span class="sxs-lookup"><span data-stu-id="f4573-102">ContinuousPhaseEstimationIteration operation</span></span>

<span data-ttu-id="f4573-103">Namespace: [Microsoft. Quantum. caracterization](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="f4573-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="f4573-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f4573-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f4573-105">Executa uma única iteração de um algoritmo de estimativa de fase iterativa (controlado de forma clássica) usando potências reais arbitrárias de um Oracle unitário.</span><span class="sxs-lookup"><span data-stu-id="f4573-105">Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using arbitrary real powers of a unitary oracle.</span></span>

```qsharp
operation ContinuousPhaseEstimationIteration (oracle : Microsoft.Quantum.Oracles.ContinuousOracle, time : Double, theta : Double, targetState : Qubit[], controlQubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="f4573-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="f4573-106">Input</span></span>

### <a name="oracle--continuousoracle"></a><span data-ttu-id="f4573-107">Oracle: [ContinuousOracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)</span><span class="sxs-lookup"><span data-stu-id="f4573-107">oracle : [ContinuousOracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)</span></span>

<span data-ttu-id="f4573-108">Operação agindo em um Double $t $ e um registro, de modo que $U ^ t $ seja aplicado ao registro fornecido, em que $U $ é o unitário cuja fase deve ser estimada e onde $t $ é o número inteiro de energia concedido ao Oracle</span><span class="sxs-lookup"><span data-stu-id="f4573-108">Operation acting on a double $t$ and a register, such that $U^t$ is applied to the given register, where $U$ is the unitary whose phase is to be estimated, and where $t$ is the integer power given to the oracle</span></span>


### <a name="time--double"></a><span data-ttu-id="f4573-109">hora: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f4573-109">time : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f4573-110">Número de vezes para aplicar o Oracle unitário fornecido.</span><span class="sxs-lookup"><span data-stu-id="f4573-110">Number of times to apply the given unitary oracle.</span></span>


### <a name="theta--double"></a><span data-ttu-id="f4573-111">teta: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f4573-111">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f4573-112">Ângulo pelo qual inverter a fase no qubit de controle antes de agir no estado de destino.</span><span class="sxs-lookup"><span data-stu-id="f4573-112">Angle by which to invert the phase on the control qubit before acting on the target state.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="f4573-113">TargetState: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="f4573-113">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="f4573-114">Registro de estado acionado pelo Oracle unitário determinado.</span><span class="sxs-lookup"><span data-stu-id="f4573-114">Register of state acted upon by the given unitary oracle.</span></span>


### <a name="controlqubit--qubit"></a><span data-ttu-id="f4573-115">controlQubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f4573-115">controlQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>





## <a name="output--unit"></a><span data-ttu-id="f4573-116">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f4573-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

