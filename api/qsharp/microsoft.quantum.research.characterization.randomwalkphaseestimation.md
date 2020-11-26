---
uid: Microsoft.Quantum.Research.Characterization.RandomWalkPhaseEstimation
title: Operação RandomWalkPhaseEstimation
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Characterization
qsharp.name: RandomWalkPhaseEstimation
qsharp.summary: Performs iterative phase estimation using a random walk to approximate Bayesian inference on the classical measurement results from a given oracle and eigenstate.
ms.openlocfilehash: 2c3afdd41da24a1f32f59f36f0f5c5ed29df1f0b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226155"
---
# <a name="randomwalkphaseestimation-operation"></a><span data-ttu-id="7b2f2-102">Operação RandomWalkPhaseEstimation</span><span class="sxs-lookup"><span data-stu-id="7b2f2-102">RandomWalkPhaseEstimation operation</span></span>

<span data-ttu-id="7b2f2-103">Namespace: [Microsoft. Quantum. Research. caracterization](xref:Microsoft.Quantum.Research.Characterization)</span><span class="sxs-lookup"><span data-stu-id="7b2f2-103">Namespace: [Microsoft.Quantum.Research.Characterization](xref:Microsoft.Quantum.Research.Characterization)</span></span>

<span data-ttu-id="7b2f2-104">Pacote: [Microsoft. Quantum. Research. caracterization](https://nuget.org/packages/Microsoft.Quantum.Research.Characterization)</span><span class="sxs-lookup"><span data-stu-id="7b2f2-104">Package: [Microsoft.Quantum.Research.Characterization](https://nuget.org/packages/Microsoft.Quantum.Research.Characterization)</span></span>


<span data-ttu-id="7b2f2-105">Executa estimativa de fase iterativa usando uma passagem aleatória para a inferência de Bayesiana aproximada nos resultados da medição clássica de um determinado Oracle e eigenstate.</span><span class="sxs-lookup"><span data-stu-id="7b2f2-105">Performs iterative phase estimation using a random walk to approximate Bayesian inference on the classical measurement results from a given oracle and eigenstate.</span></span>

```qsharp
operation RandomWalkPhaseEstimation (initialMean : Double, initialStdDev : Double, nMeasurements : Int, maxMeasurements : Int, unwind : Int, oracle : Microsoft.Quantum.Oracles.ContinuousOracle, targetState : Qubit[]) : Double
```


## <a name="input"></a><span data-ttu-id="7b2f2-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="7b2f2-106">Input</span></span>

### <a name="initialmean--double"></a><span data-ttu-id="7b2f2-107">initialMean: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="7b2f2-107">initialMean : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="7b2f2-108">Média da distribuição anterior inicial normal em relação a $ \phi $.</span><span class="sxs-lookup"><span data-stu-id="7b2f2-108">Mean of the initial normal prior distribution over $\phi$.</span></span>


### <a name="initialstddev--double"></a><span data-ttu-id="7b2f2-109">initialStdDev: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="7b2f2-109">initialStdDev : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="7b2f2-110">Desvio padrão da distribuição anterior inicial normal em relação a $ \phi $.</span><span class="sxs-lookup"><span data-stu-id="7b2f2-110">Standard deviation of the initial normal prior distribution over $\phi$.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="7b2f2-111">nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7b2f2-111">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7b2f2-112">Número de medições a serem aceitas na estimativa final de posteriores.</span><span class="sxs-lookup"><span data-stu-id="7b2f2-112">Number of measurements to be accepted into the final posterior estimate.</span></span>


### <a name="maxmeasurements--int"></a><span data-ttu-id="7b2f2-113">maxMeasurements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7b2f2-113">maxMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7b2f2-114">Número total de medições que podem ser realizadas antes que a operação seja considerada como falha.</span><span class="sxs-lookup"><span data-stu-id="7b2f2-114">Total number of measurements than can be taken before the operation is considered to have failed.</span></span>


### <a name="unwind--int"></a><span data-ttu-id="7b2f2-115">desenrolar: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7b2f2-115">unwind : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7b2f2-116">Número de resultados a serem esquecidos quando as verificações de consistência falham.</span><span class="sxs-lookup"><span data-stu-id="7b2f2-116">Number of results to forget when consistency checks fail.</span></span>


### <a name="oracle--continuousoracle"></a><span data-ttu-id="7b2f2-117">Oracle: [ContinuousOracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)</span><span class="sxs-lookup"><span data-stu-id="7b2f2-117">oracle : [ContinuousOracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)</span></span>

<span data-ttu-id="7b2f2-118">Uma operação que representa um unitário $U $ de $U (t) \ket{\phi} = e ^ {i t \phi}\ket{\phi} $ for eigenstates $ \ket{\phi} $ com fase desconhecida $ \phi na \mathbb{R} ^ + $.</span><span class="sxs-lookup"><span data-stu-id="7b2f2-118">An operation representing a unitary $U$ such that $U(t)\ket{\phi} = e^{i t \phi}\ket{\phi}$ for eigenstates $\ket{\phi}$ with unknown phase $\phi \in \mathbb{R}^+$.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="7b2f2-119">TargetState: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="7b2f2-119">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="7b2f2-120">Um registro que $U $ age.</span><span class="sxs-lookup"><span data-stu-id="7b2f2-120">A register that $U$ acts on.</span></span>



## <a name="output--double"></a><span data-ttu-id="7b2f2-121">Saída: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="7b2f2-121">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="7b2f2-122">A estimativa final $ \hat{\phi} \mathrel{: =} \expect [\phi] $, em que a expectativa é sobre o posteriores dado todos os dados aceitos.</span><span class="sxs-lookup"><span data-stu-id="7b2f2-122">The final estimate $\hat{\phi} \mathrel{:=} \expect[\phi]$ , where the expectation is over the posterior given all accepted data.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b2f2-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b2f2-123">Remarks</span></span>

### <a name="iterative-phase-estimation-and-eigenstates"></a><span data-ttu-id="7b2f2-124">Estimativa e Eigenstates de fase iterativa</span><span class="sxs-lookup"><span data-stu-id="7b2f2-124">Iterative Phase Estimation and Eigenstates</span></span>

<span data-ttu-id="7b2f2-125">Em geral, o registro de entrada `eigenstate` não precisa ser um eigenstate $ \ket{\phi} $ de $U $, mas pode ser uma superposição em relação a eigenstates.</span><span class="sxs-lookup"><span data-stu-id="7b2f2-125">In general, the input register `eigenstate` need not be an eigenstate $\ket{\phi}$ of $U$, but can be a superposition over eigenstates.</span></span> <span data-ttu-id="7b2f2-126">Suponha que o estado de entrada seja fornecido por \begin{align} \ket{\psi} & = \sum \_ {j} \alpha \_ j \ket{\phi \_ j}, \end{Align}, em que $ \{ \alpha \_ j \} $ são coeficientes complexos, de modo que $ \sum \_ j | \alpha \_ j | ^ 2 = $1 e onde $U \ket{\phi \_ j} = \phi \_ j\ket {\ Phi \_ j} $.</span><span class="sxs-lookup"><span data-stu-id="7b2f2-126">Suppose that the input state is given by \begin{align} \ket{\psi} & = \sum\_{j} \alpha\_j \ket{\phi\_j}, \end{align} where $\{\alpha\_j\}$ are complex coefficients such that $\sum\_j |\alpha\_j|^2 = 1$ and where $U\ket{\phi\_j} = \phi\_j\ket{\phi\_j}$.</span></span>

<span data-ttu-id="7b2f2-127">Em seguida, executar estimativa de fase iterativa eventualmente convergirá para um único eigenstate, conforme descrito no [Guia de desenvolvimento](xref:microsoft.quantum.libraries.characterization#iterative-phase-estimation-without-eigenstates).</span><span class="sxs-lookup"><span data-stu-id="7b2f2-127">Then, performing iterative phase estimation will eventually converge to a single eigenstate, as described in the [development guide](xref:microsoft.quantum.libraries.characterization#iterative-phase-estimation-without-eigenstates).</span></span>

### <a name="experiment-design"></a><span data-ttu-id="7b2f2-128">Design do experimento</span><span class="sxs-lookup"><span data-stu-id="7b2f2-128">Experiment Design</span></span>

<span data-ttu-id="7b2f2-129">Os tempos de medição $t $ e os ângulos de inversão $ \theta $ passados para `oracle` são escolhidos de acordo com a *heurística de adivinhação de partícula*, \Begin{align} \theta \sim \Pr (\phi), \quad t \approx \frac {1} {\variance{\phi}}.</span><span class="sxs-lookup"><span data-stu-id="7b2f2-129">The measurement times $t$ and inversion angles $\theta$ passed to `oracle` are chosen according to the *particle guess heuristic*, \begin{align} \theta \sim \Pr(\phi),\quad t \approx \frac{1}{\variance{\phi}}.</span></span>
<span data-ttu-id="7b2f2-130">\end{align} esse heurístico é ideal para reduzir a variância esperada de posteriores na estimativa de fase iterativa sob a hipótese de um normal anterior.</span><span class="sxs-lookup"><span data-stu-id="7b2f2-130">\end{align} This heuristic is optimal for reducing the expected posterior variance in iterative phase estimation under the assumption of a normal prior.</span></span>

### <a name="optimality"></a><span data-ttu-id="7b2f2-131">Ideais</span><span class="sxs-lookup"><span data-stu-id="7b2f2-131">Optimality</span></span>

<span data-ttu-id="7b2f2-132">Esta operação aproxima o estimador ideal para a fase $ \phi $, conforme avaliado usando a perda quadrática $L (\phi, \hat{\phi}) \mathrel{: =} (\phi-\hat{\phi}) ^ 2 $.</span><span class="sxs-lookup"><span data-stu-id="7b2f2-132">This operation approximates the optimal estimator for the phase $\phi$, as evaluated using the quadratic loss $L(\phi, \hat{\phi}) \mathrel{:=} (\phi - \hat{\phi})^2$.</span></span>

<span data-ttu-id="7b2f2-133">Consulte [estimativa de fase de Bayesiana](xref:microsoft.quantum.libraries.characterization#bayesian-phase-estimation) para obter mais detalhes sobre as estatísticas de estimativa de fase iterativa.</span><span class="sxs-lookup"><span data-stu-id="7b2f2-133">See [Bayesian Phase Estimation](xref:microsoft.quantum.libraries.characterization#bayesian-phase-estimation) for more details on the statistics of iterative phase estimation.</span></span>

## <a name="references"></a><span data-ttu-id="7b2f2-134">Referências</span><span class="sxs-lookup"><span data-stu-id="7b2f2-134">References</span></span>

- <span data-ttu-id="7b2f2-135">Referencial *et al.* 2011 [doi: 10/TFX](https://doi.org/10.1007/s11128-012-0407-6), [arXiv: 1110.3067](https://arxiv.org/abs/1110.3067).</span><span class="sxs-lookup"><span data-stu-id="7b2f2-135">Ferrie *et al.* 2011 [doi:10/tfx](https://doi.org/10.1007/s11128-012-0407-6), [arXiv:1110.3067](https://arxiv.org/abs/1110.3067).</span></span>
- <span data-ttu-id="7b2f2-136">Wiebe *et al.* 2013 [doi: 10/TF3](https://doi.org/10.1103/PhysRevLett.112.190501), [arXiv: 1309.0876](https://arxiv.org/abs/1309.0876)</span><span class="sxs-lookup"><span data-stu-id="7b2f2-136">Wiebe *et al.* 2013 [doi:10/tf3](https://doi.org/10.1103/PhysRevLett.112.190501), [arXiv:1309.0876](https://arxiv.org/abs/1309.0876)</span></span>
- <span data-ttu-id="7b2f2-137">Wiebe e granade 2018 *(na preparação)*.</span><span class="sxs-lookup"><span data-stu-id="7b2f2-137">Wiebe and Granade 2018 *(in preparation)*.</span></span>