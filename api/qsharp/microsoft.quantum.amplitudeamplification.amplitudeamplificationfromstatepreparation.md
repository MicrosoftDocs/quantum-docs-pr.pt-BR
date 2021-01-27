---
uid: Microsoft.Quantum.AmplitudeAmplification.AmplitudeAmplificationFromStatePreparation
title: Função AmplitudeAmplificationFromStatePreparation
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: AmplitudeAmplificationFromStatePreparation
qsharp.summary: Amplitude amplification by oracles for partial reflections.
ms.openlocfilehash: e64ad5ad4e975483f20f92c0b070dd6788ef296b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847447"
---
# <a name="amplitudeamplificationfromstatepreparation-function"></a><span data-ttu-id="fdff3-102">Função AmplitudeAmplificationFromStatePreparation</span><span class="sxs-lookup"><span data-stu-id="fdff3-102">AmplitudeAmplificationFromStatePreparation function</span></span>

<span data-ttu-id="fdff3-103">Namespace: [Microsoft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="fdff3-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="fdff3-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fdff3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fdff3-105">Amplificação de amplitude por Oracle para reflexões parciais.</span><span class="sxs-lookup"><span data-stu-id="fdff3-105">Amplitude amplification by oracles for partial reflections.</span></span>

```qsharp
function AmplitudeAmplificationFromStatePreparation (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, stateOracle : Microsoft.Quantum.Oracles.StateOracle, idxFlagQubit : Int) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="fdff3-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="fdff3-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="fdff3-107">fases: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="fdff3-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="fdff3-108">Fases de reflexos parciais</span><span class="sxs-lookup"><span data-stu-id="fdff3-108">Phases of partial reflections</span></span>


### <a name="stateoracle--stateoracle"></a><span data-ttu-id="fdff3-109">stateOracle: [stateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="fdff3-109">stateOracle : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="fdff3-110">O Oracle $A $ unitário que prepara o estado de início</span><span class="sxs-lookup"><span data-stu-id="fdff3-110">Unitary oracle $A$ that prepares start state</span></span>


### <a name="idxflagqubit--int"></a><span data-ttu-id="fdff3-111">idxFlagQubit: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="fdff3-111">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="fdff3-112">Índice para sinalizar qubit</span><span class="sxs-lookup"><span data-stu-id="fdff3-112">Index to flag qubit</span></span>



## <a name="output--qubit--unit--is-adj--ctl"></a><span data-ttu-id="fdff3-113">Saída: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="fdff3-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="fdff3-114">Uma operação que implementa amplificação de amplitude por Oracle que são implementadas por reflexões parciais.</span><span class="sxs-lookup"><span data-stu-id="fdff3-114">An operation that implements amplitude amplification by oracles that are implemented by partial reflections.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdff3-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="fdff3-115">Remarks</span></span>

<span data-ttu-id="fdff3-116">Isso impõe condições mais estritas na forma dos Estados inicial e de destino do que em `AmpAmpByReflectionPhases` .</span><span class="sxs-lookup"><span data-stu-id="fdff3-116">This imposes stricter conditions on form of the start and target states than in `AmpAmpByReflectionPhases`.</span></span>
<span data-ttu-id="fdff3-117">Supõe-se que o estado de destino seja marcado por $ \ket {1} \_ f $.</span><span class="sxs-lookup"><span data-stu-id="fdff3-117">It is assumed that the target state is marked by $\ket{1}\_f$.</span></span>
<span data-ttu-id="fdff3-118">Presume-se que \begin{align} A\ket {0} \_ {f} \ket {0} \_ s = \lambda\ket {1} \_ f\ket {\ Text {Target}} \_ s + \sqrt{1-| \lambda | ^ 2} \ket {0} \_ f\cdots, \end{align} na maioria dos casos `flagQubit` e `auxiliaryRegister` sejam inicializados no estado $ \ket {0} \_ {f} \ket {0} \_ s $.</span><span class="sxs-lookup"><span data-stu-id="fdff3-118">It is assumed that \begin{align} A\ket{0}\_{f}\ket{0}\_s= \lambda\ket{1}\_f\ket{\text{target}}\_s + \sqrt{1-|\lambda|^2}\ket{0}\_f\cdots, \end{align} In most cases, `flagQubit` and `auxiliaryRegister` are initialized in the state $\ket{0}\_{f}\ket{0}\_s$.</span></span>