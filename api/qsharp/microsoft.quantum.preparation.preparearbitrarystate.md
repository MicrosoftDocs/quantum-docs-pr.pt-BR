---
uid: Microsoft.Quantum.Preparation.PrepareArbitraryState
title: Operação PrepareArbitraryState
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareArbitraryState
qsharp.summary: >-
  > [!WARNING]

  > PrepareArbitraryState has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateCP> instead.


  Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients.
ms.openlocfilehash: 18a1e86f8e110a8f48d7dd50961e1f1f471ffc4e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96190692"
---
# <a name="preparearbitrarystate-operation"></a><span data-ttu-id="7722f-102">Operação PrepareArbitraryState</span><span class="sxs-lookup"><span data-stu-id="7722f-102">PrepareArbitraryState operation</span></span>

<span data-ttu-id="7722f-103">Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="7722f-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="7722f-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7722f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="7722f-105">PrepareArbitraryState foi preterido.</span><span class="sxs-lookup"><span data-stu-id="7722f-105">PrepareArbitraryState has been deprecated.</span></span> <span data-ttu-id="7722f-106">Use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateCP> em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="7722f-106">Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateCP> instead.</span></span>

<span data-ttu-id="7722f-107">Dado um conjunto de coeficientes e um registro de Quantum codificado little-endian, o prepara um estado nesse registro descrito pelos coeficientes fornecidos.</span><span class="sxs-lookup"><span data-stu-id="7722f-107">Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients.</span></span>

```qsharp
operation PrepareArbitraryState (coefficients : Microsoft.Quantum.Math.ComplexPolar[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="7722f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="7722f-108">Description</span></span>

<span data-ttu-id="7722f-109">Esta operação prepara um estado de Quantum arbitrário $ \ket{\psi} $ com coeficientes complexos $r _j e ^ {i t_j} $ do estado base computacional $n $-qubit $ \ket{0 \cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="7722f-109">This operation prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0 \cdots 0}$.</span></span>
<span data-ttu-id="7722f-110">Em particular, a ação dessa operação pode ser simulada pela transformação unitário $U $, que age no estado todos-zeros como</span><span class="sxs-lookup"><span data-stu-id="7722f-110">In particular, the action of this operation can be simulated by the a unitary transformation $U$ which acts on the all-zeros state as</span></span>

<span data-ttu-id="7722f-111">$ $ \begin{align} U\ket {0... 0} & = \ket{\psi} \\ \\ & = \frac{\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \ket{j}} {\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="7722f-111">$$ \begin{align} U\ket{0...0} & = \ket{\psi} \\\\ & = \frac{ \sum_{j=0}^{2^n-1} r_j e^{i t_j} \ket{j} }{ \sqrt{\sum_{j=0}^{2^n-1} |r_j|^2} }.</span></span>
<span data-ttu-id="7722f-112">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="7722f-112">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="7722f-113">Entrada</span><span class="sxs-lookup"><span data-stu-id="7722f-113">Input</span></span>

### <a name="coefficients--complexpolar"></a><span data-ttu-id="7722f-114">coeficientes: [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span><span class="sxs-lookup"><span data-stu-id="7722f-114">coefficients : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span></span>

<span data-ttu-id="7722f-115">Matriz de até $2 ^ n $ coeficientes complexos representados por seu valor absoluto e fase $ (r_j, t_j) $.</span><span class="sxs-lookup"><span data-stu-id="7722f-115">Array of up to $2^n$ complex coefficients represented by their absolute value and phase $(r_j, t_j)$.</span></span> <span data-ttu-id="7722f-116">O coeficiente $j $ th indexa o estado de número $ \ket{j} $ codificado em um formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="7722f-116">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="7722f-117">qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="7722f-117">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="7722f-118">Qubit registra os Estados de número de codificação no formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="7722f-118">Qubit register encoding number states in little-endian format.</span></span> <span data-ttu-id="7722f-119">Isso deve ser inicializado no estado de base computacional $ \ket{0...0} $.</span><span class="sxs-lookup"><span data-stu-id="7722f-119">This is expected to be initialized in the computational basis state $\ket{0...0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7722f-120">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7722f-120">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="7722f-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="7722f-121">Remarks</span></span>

<span data-ttu-id="7722f-122">Coeficientes de entrada negativas $r _j < $0 serão tratados como se positivo com o valor $ | r_j | $.</span><span class="sxs-lookup"><span data-stu-id="7722f-122">Negative input coefficients $r_j < 0$ will be treated as though positive with value $|r_j|$.</span></span> <span data-ttu-id="7722f-123">`coefficients` será preenchido com os elementos $ (r_j, t_j) = (0,0, 0,0) $ se menos de $2 ^ n $ forem especificados.</span><span class="sxs-lookup"><span data-stu-id="7722f-123">`coefficients` will be padded with elements $(r_j, t_j) = (0.0, 0.0)$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="7722f-124">Referências</span><span class="sxs-lookup"><span data-stu-id="7722f-124">References</span></span>

- <span data-ttu-id="7722f-125">Síntese de circuitos lógicos Quantum Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="7722f-125">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="7722f-126">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="7722f-126">See Also</span></span>

- [<span data-ttu-id="7722f-127">Microsoft. Quantum. Preparation. ApproximatelyPrepareArbitraryState</span><span class="sxs-lookup"><span data-stu-id="7722f-127">Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState</span></span>](xref:Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState)