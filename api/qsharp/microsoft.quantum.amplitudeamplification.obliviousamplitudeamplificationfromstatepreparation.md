---
uid: Microsoft.Quantum.AmplitudeAmplification.ObliviousAmplitudeAmplificationFromStatePreparation
title: Função ObliviousAmplitudeAmplificationFromStatePreparation
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ObliviousAmplitudeAmplificationFromStatePreparation
qsharp.summary: Oblivious amplitude amplification by oracles for partial reflections.
ms.openlocfilehash: 9975d26af8f9beb2b91e409ad78159d6f04936e3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694900"
---
# <a name="obliviousamplitudeamplificationfromstatepreparation-function"></a><span data-ttu-id="20c4a-102">Função ObliviousAmplitudeAmplificationFromStatePreparation</span><span class="sxs-lookup"><span data-stu-id="20c4a-102">ObliviousAmplitudeAmplificationFromStatePreparation function</span></span>

<span data-ttu-id="20c4a-103">Namespace: [Microsoft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="20c4a-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="20c4a-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="20c4a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="20c4a-105">Amplificação de amplitude de alheios por Oracle para reflexões parciais.</span><span class="sxs-lookup"><span data-stu-id="20c4a-105">Oblivious amplitude amplification by oracles for partial reflections.</span></span>

```qsharp
function ObliviousAmplitudeAmplificationFromStatePreparation (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle, idxFlagQubit : Int) : ((Qubit[], Qubit[]) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="20c4a-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="20c4a-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="20c4a-107">fases: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="20c4a-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="20c4a-108">Fases de reflexos parciais</span><span class="sxs-lookup"><span data-stu-id="20c4a-108">Phases of partial reflections</span></span>


### <a name="startstateoracle--deterministicstateoracle"></a><span data-ttu-id="20c4a-109">startStateOracle: [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="20c4a-109">startStateOracle : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="20c4a-110">O Oracle $A $ unitário que prepara o estado de início auxiliar</span><span class="sxs-lookup"><span data-stu-id="20c4a-110">Unitary oracle $A$ that prepares auxiliary start state</span></span>


### <a name="signaloracle--obliviousoracle"></a><span data-ttu-id="20c4a-111">signalOracle: [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span><span class="sxs-lookup"><span data-stu-id="20c4a-111">signalOracle : [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span></span>

<span data-ttu-id="20c4a-112">O $O do Oracle unitário $ do tipo `ObliviousOracle` que atua em conjunto no registro auxiliar e do sistema</span><span class="sxs-lookup"><span data-stu-id="20c4a-112">Unitary oracle $O$ of type `ObliviousOracle` that acts jointly on the auxiliary and system register</span></span>


### <a name="idxflagqubit--int"></a><span data-ttu-id="20c4a-113">idxFlagQubit: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="20c4a-113">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="20c4a-114">Índice para registro de sinalizador de qubit único</span><span class="sxs-lookup"><span data-stu-id="20c4a-114">Index to single-qubit flag register</span></span>



## <a name="output--qubitqubit--unit-adj--ctl"></a><span data-ttu-id="20c4a-115">Saída: ([qubit](xref:microsoft.quantum.lang-ref.qubit)[],[qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [unidade](xref:microsoft.quantum.lang-ref.unit) adj + CTL</span><span class="sxs-lookup"><span data-stu-id="20c4a-115">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="20c4a-116">Uma operação que implementa a amplificação de amplitude de alheios com base em reflexos parciais.</span><span class="sxs-lookup"><span data-stu-id="20c4a-116">An operation that implements oblivious amplitude amplification based on partial reflections.</span></span>

## <a name="remarks"></a><span data-ttu-id="20c4a-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="20c4a-117">Remarks</span></span>

<span data-ttu-id="20c4a-118">Isso impõe condições mais estritas na forma de inicialização auxiliar e Estados de destino do que em `AmpAmpObliviousByReflectionPhases` .</span><span class="sxs-lookup"><span data-stu-id="20c4a-118">This imposes stricter conditions on form of the auxiliary start and target states than in `AmpAmpObliviousByReflectionPhases`.</span></span>
<span data-ttu-id="20c4a-119">Supõe-se que $A \ket {0} \_ f\ket {0} \_ a = \ket{\Text{Start}} \_ {FA} $ prepara o estado de início auxiliar $ \ket{\Text{Start}} \_ {FA} $ da base computacional $ \ket {0} \_ f\ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="20c4a-119">It is assumed that $A\ket{0}\_f\ket{0}\_a= \ket{\text{start}}\_{fa}$ prepares the auxiliary start state $\ket{\text{start}}\_{fa}$ from the computational basis $\ket{0}\_f\ket{0}$.</span></span>
<span data-ttu-id="20c4a-120">Supõe-se que o estado de destino seja marcado por $ \ket {1} \_ f $.</span><span class="sxs-lookup"><span data-stu-id="20c4a-120">It is assumed that the target state is marked by $\ket{1}\_f$.</span></span>
<span data-ttu-id="20c4a-121">Supõe-se que \begin{align} O\ket {\ Text {Start}} \_ {FA} \ket{\psi} \_ s = \lambda\ket {1} \_ f\ket {\ Text {qualquer coisa}} \_ a\ket {\ Text {Target}} \_ s U \ket{\psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket {0} \_ f\cdots, \end{align} para alguns $U unitários $.</span><span class="sxs-lookup"><span data-stu-id="20c4a-121">It is assumed that \begin{align} O\ket{\text{start}}\_{fa}\ket{\psi}\_s= \lambda\ket{1}\_f\ket{\text{anything}}\_a\ket{\text{target}}\_s U \ket{\psi}\_s + \sqrt{1-|\lambda|^2}\ket{0}\_f\cdots, \end{align} for some unitary $U$.</span></span>