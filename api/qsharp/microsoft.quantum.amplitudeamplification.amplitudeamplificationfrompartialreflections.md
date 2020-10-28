---
uid: Microsoft.Quantum.AmplitudeAmplification.AmplitudeAmplificationFromPartialReflections
title: Função AmplitudeAmplificationFromPartialReflections
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: AmplitudeAmplificationFromPartialReflections
qsharp.summary: Amplitude amplification by partial reflections.
ms.openlocfilehash: fc7c2c0d05ea626f7f7e5d8ebf3ce5ecea61390b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694917"
---
# <a name="amplitudeamplificationfrompartialreflections-function"></a><span data-ttu-id="d6f64-102">Função AmplitudeAmplificationFromPartialReflections</span><span class="sxs-lookup"><span data-stu-id="d6f64-102">AmplitudeAmplificationFromPartialReflections function</span></span>

<span data-ttu-id="d6f64-103">Namespace: [Microsoft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="d6f64-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="d6f64-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d6f64-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d6f64-105">Amplificação de amplitude por reflexos parciais.</span><span class="sxs-lookup"><span data-stu-id="d6f64-105">Amplitude amplification by partial reflections.</span></span>

```qsharp
function AmplitudeAmplificationFromPartialReflections (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, targetStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="d6f64-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="d6f64-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="d6f64-107">fases: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="d6f64-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="d6f64-108">Fases de reflexos parciais</span><span class="sxs-lookup"><span data-stu-id="d6f64-108">Phases of partial reflections</span></span>


### <a name="startstatereflection--reflectionoracle"></a><span data-ttu-id="d6f64-109">startStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="d6f64-109">startStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="d6f64-110">Operador de reflexo sobre o estado inicial</span><span class="sxs-lookup"><span data-stu-id="d6f64-110">Reflection operator about start state</span></span>


### <a name="targetstatereflection--reflectionoracle"></a><span data-ttu-id="d6f64-111">targetStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="d6f64-111">targetStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="d6f64-112">Operador de reflexão sobre o estado de destino</span><span class="sxs-lookup"><span data-stu-id="d6f64-112">Reflection operator about target state</span></span>



## <a name="output--qubit--unit-adj--ctl"></a><span data-ttu-id="d6f64-113">Saída: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL</span><span class="sxs-lookup"><span data-stu-id="d6f64-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="d6f64-114">Uma operação que implementa amplificação de amplitude por reflexos parciais.</span><span class="sxs-lookup"><span data-stu-id="d6f64-114">An operation that implements amplitude amplification by partial reflections.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6f64-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6f64-115">Remarks</span></span>

<span data-ttu-id="d6f64-116">A amplificação de amplitude é um caso especial de amplificação de amplitude de alheios em que não há qubits de sistema e o alheios Oracle está definido como identidade.</span><span class="sxs-lookup"><span data-stu-id="d6f64-116">Amplitude amplification is a special case of oblivious amplitude amplification where there are no system qubits and the oblivious oracle is set to identity.</span></span>
<span data-ttu-id="d6f64-117">Na maioria dos casos, `startQubits` é inicializado no estado $ \ket{\text{start}} \_ $1, que é o $-$1 eigenstate de `startStateReflection` .</span><span class="sxs-lookup"><span data-stu-id="d6f64-117">In most cases, `startQubits` is initialized in the state $\ket{\text{start}}\_1$, which is the $-1$ eigenstate of `startStateReflection`.</span></span>