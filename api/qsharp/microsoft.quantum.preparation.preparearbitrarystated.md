---
uid: Microsoft.Quantum.Preparation.PrepareArbitraryStateD
title: Operação PrepareArbitraryStateD
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareArbitraryStateD
qsharp.summary: Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients.
ms.openlocfilehash: 61f6614821951435828cd28edeb1447cb33f3648
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842369"
---
# <a name="preparearbitrarystated-operation"></a><span data-ttu-id="808bf-102">Operação PrepareArbitraryStateD</span><span class="sxs-lookup"><span data-stu-id="808bf-102">PrepareArbitraryStateD operation</span></span>

<span data-ttu-id="808bf-103">Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="808bf-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="808bf-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="808bf-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="808bf-105">Dado um conjunto de coeficientes e um registro de Quantum codificado little-endian, o prepara um estado nesse registro descrito pelos coeficientes fornecidos.</span><span class="sxs-lookup"><span data-stu-id="808bf-105">Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients.</span></span>

```qsharp
operation PrepareArbitraryStateD (coefficients : Double[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="808bf-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="808bf-106">Description</span></span>

<span data-ttu-id="808bf-107">Esta operação prepara um estado de Quantum arbitrário $ \ket{\psi} $ com coeficientes complexos $r _j e ^ {i t_j} $ do estado base computacional $n $-qubit $ \ket{0 \cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="808bf-107">This operation prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0 \cdots 0}$.</span></span>
<span data-ttu-id="808bf-108">Em particular, a ação dessa operação pode ser simulada pela transformação unitário $U $ que age no estado todos-zeros como</span><span class="sxs-lookup"><span data-stu-id="808bf-108">In particular, the action of this operation can be simulated by the a unitary transformation $U$ that acts on the all-zeros state as</span></span>

<span data-ttu-id="808bf-109">$ $ \begin{align} U\ket {0... 0} & = \ket{\psi} \\ \\ & = \frac{\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \ket{j}} {\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="808bf-109">$$ \begin{align} U\ket{0...0} & = \ket{\psi} \\\\ & = \frac{ \sum_{j=0}^{2^n-1} r_j e^{i t_j} \ket{j} }{ \sqrt{\sum_{j=0}^{2^n-1} |r_j|^2} }.</span></span>
<span data-ttu-id="808bf-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="808bf-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="808bf-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="808bf-111">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="808bf-112">coeficientes: [duplo](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="808bf-112">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="808bf-113">Matriz de até US $2 ^ n $ reais coeficientes.</span><span class="sxs-lookup"><span data-stu-id="808bf-113">Array of up to $2^n$ real coefficients.</span></span> <span data-ttu-id="808bf-114">O coeficiente $j $ th indexa o estado de número $ \ket{j} $ codificado em um formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="808bf-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="808bf-115">qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="808bf-115">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="808bf-116">Qubit registra os Estados de número de codificação no formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="808bf-116">Qubit register encoding number states in little-endian format.</span></span> <span data-ttu-id="808bf-117">Isso deve ser inicializado no estado de base computacional $ \ket{0...0} $.</span><span class="sxs-lookup"><span data-stu-id="808bf-117">This is expected to be initialized in the computational basis state $\ket{0...0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="808bf-118">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="808bf-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="808bf-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="808bf-119">Remarks</span></span>

<span data-ttu-id="808bf-120">Coeficientes de entrada negativas $r _j < $0 serão tratados como se positivo com o valor $ | r_j | $.</span><span class="sxs-lookup"><span data-stu-id="808bf-120">Negative input coefficients $r_j < 0$ will be treated as though positive with value $|r_j|$.</span></span> <span data-ttu-id="808bf-121">`coefficients` será preenchido com os elementos $ (r_j, t_j) = (0,0, 0,0) $ se menos de $2 ^ n $ forem especificados.</span><span class="sxs-lookup"><span data-stu-id="808bf-121">`coefficients` will be padded with elements $(r_j, t_j) = (0.0, 0.0)$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="808bf-122">Referências</span><span class="sxs-lookup"><span data-stu-id="808bf-122">References</span></span>

- <span data-ttu-id="808bf-123">Síntese de circuitos lógicos Quantum Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="808bf-123">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="808bf-124">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="808bf-124">See Also</span></span>

- [<span data-ttu-id="808bf-125">Microsoft. Quantum. Preparation. ApproximatelyPrepareArbitraryState</span><span class="sxs-lookup"><span data-stu-id="808bf-125">Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState</span></span>](xref:Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState)