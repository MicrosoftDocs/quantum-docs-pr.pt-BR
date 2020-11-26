---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyObliviousAmplitudeAmplification
title: Operação ApplyObliviousAmplitudeAmplification
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyObliviousAmplitudeAmplification
qsharp.summary: Oblivious amplitude amplification by specifying partial reflections.
ms.openlocfilehash: 9b0060201bcdae02a207362a753a0a403cdbb896
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191509"
---
# <a name="applyobliviousamplitudeamplification-operation"></a><span data-ttu-id="bdc22-102">Operação ApplyObliviousAmplitudeAmplification</span><span class="sxs-lookup"><span data-stu-id="bdc22-102">ApplyObliviousAmplitudeAmplification operation</span></span>

<span data-ttu-id="bdc22-103">Namespace: [Microsoft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="bdc22-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="bdc22-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bdc22-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bdc22-105">Amplificação de amplitude de alheios especificando reflexões parciais.</span><span class="sxs-lookup"><span data-stu-id="bdc22-105">Oblivious amplitude amplification by specifying partial reflections.</span></span>

```qsharp
operation ApplyObliviousAmplitudeAmplification (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, targetStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle, auxiliaryRegister : Qubit[], systemRegister : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="bdc22-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="bdc22-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="bdc22-107">fases: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="bdc22-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="bdc22-108">Fases de reflexos parciais</span><span class="sxs-lookup"><span data-stu-id="bdc22-108">Phases of partial reflections</span></span>


### <a name="startstatereflection--reflectionoracle"></a><span data-ttu-id="bdc22-109">startStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="bdc22-109">startStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="bdc22-110">Operador de reflexo sobre o estado de início do registro auxiliar</span><span class="sxs-lookup"><span data-stu-id="bdc22-110">Reflection operator about start state of auxiliary register</span></span>


### <a name="targetstatereflection--reflectionoracle"></a><span data-ttu-id="bdc22-111">targetStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="bdc22-111">targetStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="bdc22-112">Operador de reflexão sobre o estado de destino do registro auxiliar</span><span class="sxs-lookup"><span data-stu-id="bdc22-112">Reflection operator about target state of auxiliary register</span></span>


### <a name="signaloracle--obliviousoracle"></a><span data-ttu-id="bdc22-113">signalOracle: [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span><span class="sxs-lookup"><span data-stu-id="bdc22-113">signalOracle : [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span></span>

<span data-ttu-id="bdc22-114">O $O do Oracle unitário $ do tipo `ObliviousOracle` que atua em conjunto nos registros auxiliares e do sistema.</span><span class="sxs-lookup"><span data-stu-id="bdc22-114">Unitary oracle $O$ of type `ObliviousOracle` that acts jointly on the auxiliary and system registers.</span></span>


### <a name="auxiliaryregister--qubit"></a><span data-ttu-id="bdc22-115">auxiliaryRegister: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="bdc22-115">auxiliaryRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="bdc22-116">Registro auxiliar</span><span class="sxs-lookup"><span data-stu-id="bdc22-116">Auxiliary register</span></span>


### <a name="systemregister--qubit"></a><span data-ttu-id="bdc22-117">systemRegister: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="bdc22-117">systemRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="bdc22-118">Registro do sistema</span><span class="sxs-lookup"><span data-stu-id="bdc22-118">System register</span></span>



## <a name="output--unit"></a><span data-ttu-id="bdc22-119">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bdc22-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="bdc22-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="bdc22-120">Remarks</span></span>

<span data-ttu-id="bdc22-121">Dado um estado de início auxiliar específico $ \ket{\Text{Start}} \_ a $, um estado de destino auxiliar específico $ \ket{\Text{Target}} \_ a $ e qualquer estado do sistema $ \ket{\psi} \_ s $, suponha que \begin{align} O\ket {\ Text {Start}} \_ a\ket {\ psi} \_ s = \lambda\ket{\Text{Target}} \_ a U \ket{\psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket{\text{target} ^ \perp} \_ a\cdots \end{align} para alguns $U unitários $.</span><span class="sxs-lookup"><span data-stu-id="bdc22-121">Given a particular auxiliary start state $\ket{\text{start}}\_a$, a particular auxiliary target state $\ket{\text{target}}\_a$, and any system state $\ket{\psi}\_s$, suppose that \begin{align} O\ket{\text{start}}\_a\ket{\psi}\_s= \lambda\ket{\text{target}}\_a U \ket{\psi}\_s + \sqrt{1-|\lambda|^2}\ket{\text{target}^\perp}\_a\cdots \end{align} for some unitary $U$.</span></span>
<span data-ttu-id="bdc22-122">Por uma sequência de reflexos sobre os Estados de início e de destino no registro auxiliar intercalado por aplicativos do `signalOracle` e seu adjacente, a probabilidade de êxito da aplicação de U pode ser alterada.</span><span class="sxs-lookup"><span data-stu-id="bdc22-122">By a sequence of reflections about the start and target states on the auxiliary register interleaved by applications of `signalOracle` and its adjoint, the success probability of applying U may be altered.</span></span>

<span data-ttu-id="bdc22-123">Na maioria dos casos, `auxiliaryRegister` é inicializado no estado $ \ket{\Text{Start}} \_ a $.</span><span class="sxs-lookup"><span data-stu-id="bdc22-123">In most cases, `auxiliaryRegister` is initialized in the state $\ket{\text{start}}\_a$.</span></span>

## <a name="references"></a><span data-ttu-id="bdc22-124">Referências</span><span class="sxs-lookup"><span data-stu-id="bdc22-124">References</span></span>

<span data-ttu-id="bdc22-125">Consulte</span><span class="sxs-lookup"><span data-stu-id="bdc22-125">See</span></span>

- <span data-ttu-id="bdc22-126">[ *D.W. Berry, am Childs, r. Cleve, r. Kothari, R.D. Somma*](https://arxiv.org/abs/1312.1414) para a versão padrão.</span><span class="sxs-lookup"><span data-stu-id="bdc22-126">[ *D.W. Berry, A.M. Childs, R. Cleve, R. Kothari, R.D. Somma* ](https://arxiv.org/abs/1312.1414) for the standard version.</span></span>
  <span data-ttu-id="bdc22-127">Consulte</span><span class="sxs-lookup"><span data-stu-id="bdc22-127">See</span></span>
- <span data-ttu-id="bdc22-128">[ *G.H. Low, I.L. Chuang*](https://arxiv.org/abs/1610.06546) para uma generalização até reflexões parciais.</span><span class="sxs-lookup"><span data-stu-id="bdc22-128">[ *G.H. Low, I.L. Chuang* ](https://arxiv.org/abs/1610.06546) for a generalization to partial reflections.</span></span>