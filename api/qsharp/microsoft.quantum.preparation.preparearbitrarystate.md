---
uid: Microsoft.Quantum.Preparation.PrepareArbitraryState
title: Operação PrepareArbitraryState
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareArbitraryState
qsharp.summary: Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients.
ms.openlocfilehash: 18f45da601b02fc5f83936b086323e31a66fc20b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696886"
---
# <a name="preparearbitrarystate-operation"></a><span data-ttu-id="9cb0c-102">Operação PrepareArbitraryState</span><span class="sxs-lookup"><span data-stu-id="9cb0c-102">PrepareArbitraryState operation</span></span>

<span data-ttu-id="9cb0c-103">Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="9cb0c-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="9cb0c-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9cb0c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9cb0c-105">Dado um conjunto de coeficientes e um registro de Quantum codificado little-endian, o prepara um estado nesse registro descrito pelos coeficientes fornecidos.</span><span class="sxs-lookup"><span data-stu-id="9cb0c-105">Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients.</span></span>

```qsharp
operation PrepareArbitraryState (coefficients : Microsoft.Quantum.Math.ComplexPolar[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="9cb0c-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="9cb0c-106">Description</span></span>

<span data-ttu-id="9cb0c-107">Esta operação prepara um estado de Quantum arbitrário $ \ket{\psi} $ com coeficientes complexos $r _j e ^ {i t_j} $ do estado base computacional $n $-qubit $ \ket{0 \cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="9cb0c-107">This operation prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0 \cdots 0}$.</span></span>
<span data-ttu-id="9cb0c-108">Em particular, a ação dessa operação pode ser simulada pela transformação unitário $U $, que age no estado todos-zeros como</span><span class="sxs-lookup"><span data-stu-id="9cb0c-108">In particular, the action of this operation can be simulated by the a unitary transformation $U$ which acts on the all-zeros state as</span></span>

<span data-ttu-id="9cb0c-109">$ $ \begin{align} U\ket {0... 0} & = \ket{\psi} \\ \\ & = \frac{\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \ket{j}} {\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="9cb0c-109">$$ \begin{align} U\ket{0...0} & = \ket{\psi} \\\\ & = \frac{ \sum_{j=0}^{2^n-1} r_j e^{i t_j} \ket{j} }{ \sqrt{\sum_{j=0}^{2^n-1} |r_j|^2} }.</span></span>
<span data-ttu-id="9cb0c-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="9cb0c-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="9cb0c-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="9cb0c-111">Input</span></span>

### <a name="coefficients--complexpolar"></a><span data-ttu-id="9cb0c-112">coeficientes: [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span><span class="sxs-lookup"><span data-stu-id="9cb0c-112">coefficients : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span></span>

<span data-ttu-id="9cb0c-113">Matriz de até $2 ^ n $ coeficientes complexos representados por seu valor absoluto e fase $ (r_j, t_j) $.</span><span class="sxs-lookup"><span data-stu-id="9cb0c-113">Array of up to $2^n$ complex coefficients represented by their absolute value and phase $(r_j, t_j)$.</span></span> <span data-ttu-id="9cb0c-114">O coeficiente $j $ th indexa o estado de número $ \ket{j} $ codificado em um formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="9cb0c-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="9cb0c-115">qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="9cb0c-115">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="9cb0c-116">Qubit registra os Estados de número de codificação no formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="9cb0c-116">Qubit register encoding number states in little-endian format.</span></span> <span data-ttu-id="9cb0c-117">Isso deve ser inicializado no estado de base computacional $ \ket{0...0} $.</span><span class="sxs-lookup"><span data-stu-id="9cb0c-117">This is expected to be initialized in the computational basis state $\ket{0...0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9cb0c-118">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9cb0c-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="9cb0c-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="9cb0c-119">Remarks</span></span>

<span data-ttu-id="9cb0c-120">Coeficientes de entrada negativas $r _j < $0 serão tratados como se positivo com o valor $ | r_j | $.</span><span class="sxs-lookup"><span data-stu-id="9cb0c-120">Negative input coefficients $r_j < 0$ will be treated as though positive with value $|r_j|$.</span></span> <span data-ttu-id="9cb0c-121">`coefficients` será preenchido com os elementos $ (r_j, t_j) = (0,0, 0,0) $ se menos de $2 ^ n $ forem especificados.</span><span class="sxs-lookup"><span data-stu-id="9cb0c-121">`coefficients` will be padded with elements $(r_j, t_j) = (0.0, 0.0)$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="9cb0c-122">Referências</span><span class="sxs-lookup"><span data-stu-id="9cb0c-122">References</span></span>

- <span data-ttu-id="9cb0c-123">Síntese de circuitos lógicos Quantum Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="9cb0c-123">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="9cb0c-124">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="9cb0c-124">See Also</span></span>

- [<span data-ttu-id="9cb0c-125">Microsoft. Quantum. Preparation. ApproximatelyPrepareArbitraryState</span><span class="sxs-lookup"><span data-stu-id="9cb0c-125">Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState</span></span>](xref:Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState)