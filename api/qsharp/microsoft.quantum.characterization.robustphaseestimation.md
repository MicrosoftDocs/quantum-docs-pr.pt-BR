---
uid: Microsoft.Quantum.Characterization.RobustPhaseEstimation
title: Operação RobustPhaseEstimation
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: RobustPhaseEstimation
qsharp.summary: Performs the robust non-iterative quantum phase estimation algorithm for a given oracle `U` and eigenstate, and provides a single real-valued estimate of the phase with variance scaling at the Heisenberg limit.
ms.openlocfilehash: 3e6774e2fe348668840cdc08fe3a070ec3d82a6d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216074"
---
# <a name="robustphaseestimation-operation"></a><span data-ttu-id="0a2ef-102">Operação RobustPhaseEstimation</span><span class="sxs-lookup"><span data-stu-id="0a2ef-102">RobustPhaseEstimation operation</span></span>

<span data-ttu-id="0a2ef-103">Namespace: [Microsoft. Quantum. caracterization](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="0a2ef-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="0a2ef-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0a2ef-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0a2ef-105">Executa o algoritmo de estimativa de fase de Quantum não iterativa robusto para um determinado Oracle `U` e eigenstate e fornece uma única estimativa de valor real da fase com dimensionamento de variação no limite de Heisenberg.</span><span class="sxs-lookup"><span data-stu-id="0a2ef-105">Performs the robust non-iterative quantum phase estimation algorithm for a given oracle `U` and eigenstate, and provides a single real-valued estimate of the phase with variance scaling at the Heisenberg limit.</span></span>

```qsharp
operation RobustPhaseEstimation (bitsPrecision : Int, oracle : Microsoft.Quantum.Oracles.DiscreteOracle, targetState : Qubit[]) : Double
```


## <a name="input"></a><span data-ttu-id="0a2ef-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="0a2ef-106">Input</span></span>

### <a name="bitsprecision--int"></a><span data-ttu-id="0a2ef-107">bitsPrecision: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0a2ef-107">bitsPrecision : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0a2ef-108">Isso fornece uma estimativa de $ \phi $ com o desvio padrão $ \sigma \le 2 \ pi/2 ^ \text{bitsPrecision} $ usando várias consultas dimensionando como $ \sigma \le 10,7 \pi/\Text{# de consultas} $.</span><span class="sxs-lookup"><span data-stu-id="0a2ef-108">This provides an estimate of $\phi$ with standard deviation $\sigma \le 2\pi / 2^\text{bitsPrecision}$ using a number of queries scaling like $\sigma \le 10.7 \pi / \text{# of queries}$.</span></span>


### <a name="oracle--discreteoracle"></a><span data-ttu-id="0a2ef-109">Oracle: [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span><span class="sxs-lookup"><span data-stu-id="0a2ef-109">oracle : [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span></span>

<span data-ttu-id="0a2ef-110">Uma operação que implementa $U ^ m $ para potências de inteiros fornecidas $m $.</span><span class="sxs-lookup"><span data-stu-id="0a2ef-110">An operation implementing $U^m$ for given integer powers $m$.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="0a2ef-111">TargetState: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="0a2ef-111">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="0a2ef-112">Uma Quantum registra que $U $ age.</span><span class="sxs-lookup"><span data-stu-id="0a2ef-112">A quantum register that $U$ acts on.</span></span> <span data-ttu-id="0a2ef-113">Se ele armazenar um eigenstate $ \ket{\phi} $ de $U $, $U \ket{\phi} = e ^ {i\phi} \ket{\phi} $ para $ \phi\in (-\pi, \pi] $ uma fase desconhecida.</span><span class="sxs-lookup"><span data-stu-id="0a2ef-113">If it stores an eigenstate $\ket{\phi}$ of $U$, then $U\ket{\phi} = e^{i\phi} \ket{\phi}$ for $\phi\in(-\pi,\pi]$ an unknown phase.</span></span>



## <a name="output--double"></a><span data-ttu-id="0a2ef-114">Saída: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="0a2ef-114">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="0a2ef-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a2ef-115">Remarks</span></span>

<span data-ttu-id="0a2ef-116">No limite de um grande número de consultas, Cramer-Rao limites inferiores para o desvio padrão da estimativa de $ \phi $ satisfazem $ \sigma \ge 2 \pi/\Text{# de consultas} $.</span><span class="sxs-lookup"><span data-stu-id="0a2ef-116">In the limit of a large number of queries, Cramer-Rao lower bounds for the standard deviation of the estimate of $\phi$ satisfy $\sigma \ge 2 \pi / \text{# of queries}$.</span></span>

## <a name="references"></a><span data-ttu-id="0a2ef-117">Referências</span><span class="sxs-lookup"><span data-stu-id="0a2ef-117">References</span></span>

- <span data-ttu-id="0a2ef-118">Calibragem robusta de um Single-Qubit universal Gate-Set por meio da estimativa de fase robusta Shelby Kimmel, Guang Hao Low, Theodore J. Yoder https://arxiv.org/abs/1502.02677</span><span class="sxs-lookup"><span data-stu-id="0a2ef-118">Robust Calibration of a Universal Single-Qubit Gate-Set via Robust Phase Estimation Shelby Kimmel, Guang Hao Low, Theodore J. Yoder https://arxiv.org/abs/1502.02677</span></span>