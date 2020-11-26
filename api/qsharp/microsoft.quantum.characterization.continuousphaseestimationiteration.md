---
uid: Microsoft.Quantum.Characterization.ContinuousPhaseEstimationIteration
title: Operação ContinuousPhaseEstimationIteration
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: ContinuousPhaseEstimationIteration
qsharp.summary: Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using arbitrary real powers of a unitary oracle.
ms.openlocfilehash: 3c0f6cf084311598346b25dd7028e290946cd87f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216278"
---
# <a name="continuousphaseestimationiteration-operation"></a><span data-ttu-id="8b328-102">Operação ContinuousPhaseEstimationIteration</span><span class="sxs-lookup"><span data-stu-id="8b328-102">ContinuousPhaseEstimationIteration operation</span></span>

<span data-ttu-id="8b328-103">Namespace: [Microsoft. Quantum. caracterization](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="8b328-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="8b328-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8b328-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8b328-105">Executa uma única iteração de um algoritmo de estimativa de fase iterativa (controlado de forma clássica) usando potências reais arbitrárias de um Oracle unitário.</span><span class="sxs-lookup"><span data-stu-id="8b328-105">Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using arbitrary real powers of a unitary oracle.</span></span>

```qsharp
operation ContinuousPhaseEstimationIteration (oracle : Microsoft.Quantum.Oracles.ContinuousOracle, time : Double, theta : Double, targetState : Qubit[], controlQubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="8b328-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="8b328-106">Input</span></span>

### <a name="oracle--continuousoracle"></a><span data-ttu-id="8b328-107">Oracle: [ContinuousOracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)</span><span class="sxs-lookup"><span data-stu-id="8b328-107">oracle : [ContinuousOracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)</span></span>

<span data-ttu-id="8b328-108">Operação agindo em um Double $t $ e um registro, de modo que $U ^ t $ seja aplicado ao registro fornecido, em que $U $ é o unitário cuja fase deve ser estimada e onde $t $ é o número inteiro de energia concedido ao Oracle</span><span class="sxs-lookup"><span data-stu-id="8b328-108">Operation acting on a double $t$ and a register, such that $U^t$ is applied to the given register, where $U$ is the unitary whose phase is to be estimated, and where $t$ is the integer power given to the oracle</span></span>


### <a name="time--double"></a><span data-ttu-id="8b328-109">hora: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8b328-109">time : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8b328-110">Número de vezes para aplicar o Oracle unitário fornecido.</span><span class="sxs-lookup"><span data-stu-id="8b328-110">Number of times to apply the given unitary oracle.</span></span>


### <a name="theta--double"></a><span data-ttu-id="8b328-111">teta: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8b328-111">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8b328-112">Ângulo pelo qual inverter a fase no qubit de controle antes de agir no estado de destino.</span><span class="sxs-lookup"><span data-stu-id="8b328-112">Angle by which to invert the phase on the control qubit before acting on the target state.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="8b328-113">TargetState: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="8b328-113">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="8b328-114">Registro de estado acionado pelo Oracle unitário determinado.</span><span class="sxs-lookup"><span data-stu-id="8b328-114">Register of state acted upon by the given unitary oracle.</span></span>


### <a name="controlqubit--qubit"></a><span data-ttu-id="8b328-115">controlQubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="8b328-115">controlQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>





## <a name="output--unit"></a><span data-ttu-id="8b328-116">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8b328-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

