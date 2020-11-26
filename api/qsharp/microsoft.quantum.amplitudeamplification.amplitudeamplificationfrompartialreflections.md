---
uid: Microsoft.Quantum.AmplitudeAmplification.AmplitudeAmplificationFromPartialReflections
title: Função AmplitudeAmplificationFromPartialReflections
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: AmplitudeAmplificationFromPartialReflections
qsharp.summary: Amplitude amplification by partial reflections.
ms.openlocfilehash: 8fa6db7d5616f8c561191e3da00a69b05041b279
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191678"
---
# <a name="amplitudeamplificationfrompartialreflections-function"></a><span data-ttu-id="07fd8-102">Função AmplitudeAmplificationFromPartialReflections</span><span class="sxs-lookup"><span data-stu-id="07fd8-102">AmplitudeAmplificationFromPartialReflections function</span></span>

<span data-ttu-id="07fd8-103">Namespace: [Microsoft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="07fd8-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="07fd8-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="07fd8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="07fd8-105">Amplificação de amplitude por reflexos parciais.</span><span class="sxs-lookup"><span data-stu-id="07fd8-105">Amplitude amplification by partial reflections.</span></span>

```qsharp
function AmplitudeAmplificationFromPartialReflections (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, targetStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="07fd8-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="07fd8-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="07fd8-107">fases: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="07fd8-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="07fd8-108">Fases de reflexos parciais</span><span class="sxs-lookup"><span data-stu-id="07fd8-108">Phases of partial reflections</span></span>


### <a name="startstatereflection--reflectionoracle"></a><span data-ttu-id="07fd8-109">startStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="07fd8-109">startStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="07fd8-110">Operador de reflexo sobre o estado inicial</span><span class="sxs-lookup"><span data-stu-id="07fd8-110">Reflection operator about start state</span></span>


### <a name="targetstatereflection--reflectionoracle"></a><span data-ttu-id="07fd8-111">targetStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="07fd8-111">targetStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="07fd8-112">Operador de reflexão sobre o estado de destino</span><span class="sxs-lookup"><span data-stu-id="07fd8-112">Reflection operator about target state</span></span>



## <a name="output--qubit--unit--is-adj--ctl"></a><span data-ttu-id="07fd8-113">Saída: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="07fd8-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="07fd8-114">Uma operação que implementa amplificação de amplitude por reflexos parciais.</span><span class="sxs-lookup"><span data-stu-id="07fd8-114">An operation that implements amplitude amplification by partial reflections.</span></span>

## <a name="remarks"></a><span data-ttu-id="07fd8-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="07fd8-115">Remarks</span></span>

<span data-ttu-id="07fd8-116">A amplificação de amplitude é um caso especial de amplificação de amplitude de alheios em que não há qubits de sistema e o alheios Oracle está definido como identidade.</span><span class="sxs-lookup"><span data-stu-id="07fd8-116">Amplitude amplification is a special case of oblivious amplitude amplification where there are no system qubits and the oblivious oracle is set to identity.</span></span>
<span data-ttu-id="07fd8-117">Na maioria dos casos, `startQubits` é inicializado no estado $ \ket{\text{start}} \_ $1, que é o $-$1 eigenstate de `startStateReflection` .</span><span class="sxs-lookup"><span data-stu-id="07fd8-117">In most cases, `startQubits` is initialized in the state $\ket{\text{start}}\_1$, which is the $-1$ eigenstate of `startStateReflection`.</span></span>