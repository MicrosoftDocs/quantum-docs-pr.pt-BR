---
uid: Microsoft.Quantum.AmplitudeAmplification.AmplitudeAmplificationFromStatePreparation
title: Função AmplitudeAmplificationFromStatePreparation
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: AmplitudeAmplificationFromStatePreparation
qsharp.summary: Amplitude amplification by oracles for partial reflections.
ms.openlocfilehash: 7725ff327e327578ff36242a2b1bc6d03fab0d0c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694916"
---
# <a name="amplitudeamplificationfromstatepreparation-function"></a><span data-ttu-id="7d471-102">Função AmplitudeAmplificationFromStatePreparation</span><span class="sxs-lookup"><span data-stu-id="7d471-102">AmplitudeAmplificationFromStatePreparation function</span></span>

<span data-ttu-id="7d471-103">Namespace: [Microsoft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="7d471-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="7d471-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7d471-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7d471-105">Amplificação de amplitude por Oracle para reflexões parciais.</span><span class="sxs-lookup"><span data-stu-id="7d471-105">Amplitude amplification by oracles for partial reflections.</span></span>

```qsharp
function AmplitudeAmplificationFromStatePreparation (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, stateOracle : Microsoft.Quantum.Oracles.StateOracle, idxFlagQubit : Int) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="7d471-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="7d471-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="7d471-107">fases: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="7d471-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="7d471-108">Fases de reflexos parciais</span><span class="sxs-lookup"><span data-stu-id="7d471-108">Phases of partial reflections</span></span>


### <a name="stateoracle--stateoracle"></a><span data-ttu-id="7d471-109">stateOracle: [stateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="7d471-109">stateOracle : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="7d471-110">O Oracle $A $ unitário que prepara o estado de início</span><span class="sxs-lookup"><span data-stu-id="7d471-110">Unitary oracle $A$ that prepares start state</span></span>


### <a name="idxflagqubit--int"></a><span data-ttu-id="7d471-111">idxFlagQubit: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7d471-111">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7d471-112">Índice para sinalizar qubit</span><span class="sxs-lookup"><span data-stu-id="7d471-112">Index to flag qubit</span></span>



## <a name="output--qubit--unit-adj--ctl"></a><span data-ttu-id="7d471-113">Saída: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL</span><span class="sxs-lookup"><span data-stu-id="7d471-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="7d471-114">Uma operação que implementa amplificação de amplitude por Oracle que são implementadas por reflexões parciais.</span><span class="sxs-lookup"><span data-stu-id="7d471-114">An operation that implements amplitude amplification by oracles that are implemented by partial reflections.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d471-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d471-115">Remarks</span></span>

<span data-ttu-id="7d471-116">Isso impõe condições mais estritas na forma dos Estados inicial e de destino do que em `AmpAmpByReflectionPhases` .</span><span class="sxs-lookup"><span data-stu-id="7d471-116">This imposes stricter conditions on form of the start and target states than in `AmpAmpByReflectionPhases`.</span></span>
<span data-ttu-id="7d471-117">Supõe-se que o estado de destino seja marcado por $ \ket {1} \_ f $.</span><span class="sxs-lookup"><span data-stu-id="7d471-117">It is assumed that the target state is marked by $\ket{1}\_f$.</span></span>
<span data-ttu-id="7d471-118">Presume-se que \begin{align} A\ket {0} \_ {f} \ket {0} \_ s = \lambda\ket {1} \_ f\ket {\ Text {Target}} \_ s + \sqrt{1-| \lambda | ^ 2} \ket {0} \_ f\cdots, \end{align} na maioria dos casos `flagQubit` e `auxiliaryRegister` sejam inicializados no estado $ \ket {0} \_ {f} \ket {0} \_ s $.</span><span class="sxs-lookup"><span data-stu-id="7d471-118">It is assumed that \begin{align} A\ket{0}\_{f}\ket{0}\_s= \lambda\ket{1}\_f\ket{\text{target}}\_s + \sqrt{1-|\lambda|^2}\ket{0}\_f\cdots, \end{align} In most cases, `flagQubit` and `auxiliaryRegister` are initialized in the state $\ket{0}\_{f}\ket{0}\_s$.</span></span>