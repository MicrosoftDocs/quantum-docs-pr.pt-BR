---
uid: Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState
title: Operação ApproximatelyPrepareArbitraryState
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: ApproximatelyPrepareArbitraryState
qsharp.summary: Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients, up to a given approximation tolerance.
ms.openlocfilehash: 2561b098c5faf2d24bb9ab348fb052025808e441
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696892"
---
# <a name="approximatelypreparearbitrarystate-operation"></a><span data-ttu-id="2c7f5-102">Operação ApproximatelyPrepareArbitraryState</span><span class="sxs-lookup"><span data-stu-id="2c7f5-102">ApproximatelyPrepareArbitraryState operation</span></span>

<span data-ttu-id="2c7f5-103">Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="2c7f5-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="2c7f5-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2c7f5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2c7f5-105">Dado um conjunto de coeficientes e um registro de Quantum codificado little-endian, o prepara um estado nesse registro descrito pelos coeficientes fornecidos, até uma determinada tolerância a uma aproximação.</span><span class="sxs-lookup"><span data-stu-id="2c7f5-105">Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients, up to a given approximation tolerance.</span></span>

```qsharp
operation ApproximatelyPrepareArbitraryState (tolerance : Double, coefficients : Microsoft.Quantum.Math.ComplexPolar[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="2c7f5-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="2c7f5-106">Description</span></span>

<span data-ttu-id="2c7f5-107">Esta operação prepara um estado de Quantum arbitrário $ \ket{\psi} $ com coeficientes complexos $r _j e ^ {i t_j} $ do estado base computacional $n $-qubit $ \ket{0 \cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="2c7f5-107">This operation prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0 \cdots 0}$.</span></span>
<span data-ttu-id="2c7f5-108">Em particular, a ação dessa operação pode ser simulada pela transformação unitário $U $, que age no estado todos-zeros como</span><span class="sxs-lookup"><span data-stu-id="2c7f5-108">In particular, the action of this operation can be simulated by the a unitary transformation $U$ which acts on the all-zeros state as</span></span>

<span data-ttu-id="2c7f5-109">$ $ \begin{align} U\ket {0... 0} & = \ket{\psi} \\ \\ & = \frac{\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \ket{j}} {\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="2c7f5-109">$$ \begin{align} U\ket{0...0} & = \ket{\psi} \\\\ & = \frac{ \sum_{j=0}^{2^n-1} r_j e^{i t_j} \ket{j} }{ \sqrt{\sum_{j=0}^{2^n-1} |r_j|^2} }.</span></span>
<span data-ttu-id="2c7f5-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="2c7f5-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="2c7f5-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="2c7f5-111">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="2c7f5-112">tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2c7f5-112">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="2c7f5-113">A tolerância de aproximação a ser usada ao preparar o estado fornecido.</span><span class="sxs-lookup"><span data-stu-id="2c7f5-113">The approximation tolerance to be used when preparing the given state.</span></span>


### <a name="coefficients--complexpolar"></a><span data-ttu-id="2c7f5-114">coeficientes: [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span><span class="sxs-lookup"><span data-stu-id="2c7f5-114">coefficients : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span></span>

<span data-ttu-id="2c7f5-115">Matriz de até $2 ^ n $ coeficientes complexos representados por seu valor absoluto e fase $ (r_j, t_j) $.</span><span class="sxs-lookup"><span data-stu-id="2c7f5-115">Array of up to $2^n$ complex coefficients represented by their absolute value and phase $(r_j, t_j)$.</span></span> <span data-ttu-id="2c7f5-116">O coeficiente $j $ th indexa o estado de número $ \ket{j} $ codificado em um formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="2c7f5-116">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="2c7f5-117">qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="2c7f5-117">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="2c7f5-118">Qubit registra os Estados de número de codificação no formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="2c7f5-118">Qubit register encoding number states in little-endian format.</span></span> <span data-ttu-id="2c7f5-119">Isso deve ser inicializado no estado de base computacional $ \ket{0...0} $.</span><span class="sxs-lookup"><span data-stu-id="2c7f5-119">This is expected to be initialized in the computational basis state $\ket{0...0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2c7f5-120">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2c7f5-120">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="2c7f5-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c7f5-121">Remarks</span></span>

<span data-ttu-id="2c7f5-122">Coeficientes de entrada negativas $r _j < $0 serão tratados como se positivo com o valor $ | r_j | $.</span><span class="sxs-lookup"><span data-stu-id="2c7f5-122">Negative input coefficients $r_j < 0$ will be treated as though positive with value $|r_j|$.</span></span> <span data-ttu-id="2c7f5-123">`coefficients` será preenchido com os elementos $ (r_j, t_j) = (0,0, 0,0) $ se menos de $2 ^ n $ forem especificados.</span><span class="sxs-lookup"><span data-stu-id="2c7f5-123">`coefficients` will be padded with elements $(r_j, t_j) = (0.0, 0.0)$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="2c7f5-124">Referências</span><span class="sxs-lookup"><span data-stu-id="2c7f5-124">References</span></span>

- <span data-ttu-id="2c7f5-125">Síntese de circuitos lógicos Quantum Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="2c7f5-125">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="2c7f5-126">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="2c7f5-126">See Also</span></span>

- [<span data-ttu-id="2c7f5-127">Microsoft. Quantum. Preparation. ApproximatelyPrepareArbitraryState</span><span class="sxs-lookup"><span data-stu-id="2c7f5-127">Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState</span></span>](xref:Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState)