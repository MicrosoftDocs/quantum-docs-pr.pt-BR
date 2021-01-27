---
uid: Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryStateD
title: Operação ApproximatelyPrepareArbitraryStateD
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: ApproximatelyPrepareArbitraryStateD
qsharp.summary: Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients, up to a given approximation tolerance.
ms.openlocfilehash: a818ada509bcb34682ac1230eb508f0b71b5d019
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842459"
---
# <a name="approximatelypreparearbitrarystated-operation"></a><span data-ttu-id="2f46c-102">Operação ApproximatelyPrepareArbitraryStateD</span><span class="sxs-lookup"><span data-stu-id="2f46c-102">ApproximatelyPrepareArbitraryStateD operation</span></span>

<span data-ttu-id="2f46c-103">Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="2f46c-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="2f46c-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2f46c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2f46c-105">Dado um conjunto de coeficientes e um registro de Quantum codificado little-endian, o prepara um estado nesse registro descrito pelos coeficientes fornecidos, até uma determinada tolerância a uma aproximação.</span><span class="sxs-lookup"><span data-stu-id="2f46c-105">Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients, up to a given approximation tolerance.</span></span>

```qsharp
operation ApproximatelyPrepareArbitraryStateD (tolerance : Double, coefficients : Double[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="2f46c-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="2f46c-106">Description</span></span>

<span data-ttu-id="2f46c-107">Esta operação prepara um estado de Quantum arbitrário $ \ket{\psi} $ com coeficientes complexos $r _j e ^ {i t_j} $ do estado base computacional $n $-qubit $ \ket{0 \cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="2f46c-107">This operation prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0 \cdots 0}$.</span></span>
<span data-ttu-id="2f46c-108">Em particular, a ação dessa operação pode ser simulada pela transformação unitário $U $, que age no estado todos-zeros como</span><span class="sxs-lookup"><span data-stu-id="2f46c-108">In particular, the action of this operation can be simulated by the a unitary transformation $U$ which acts on the all-zeros state as</span></span>

<span data-ttu-id="2f46c-109">$ $ \begin{align} U\ket {0... 0} & = \ket{\psi} \\ \\ & = \frac{\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \ket{j}} {\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="2f46c-109">$$ \begin{align} U\ket{0...0} & = \ket{\psi} \\\\ & = \frac{ \sum_{j=0}^{2^n-1} r_j e^{i t_j} \ket{j} }{ \sqrt{\sum_{j=0}^{2^n-1} |r_j|^2} }.</span></span>
<span data-ttu-id="2f46c-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="2f46c-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="2f46c-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="2f46c-111">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="2f46c-112">tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2f46c-112">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="2f46c-113">A tolerância de aproximação a ser usada ao preparar o estado fornecido.</span><span class="sxs-lookup"><span data-stu-id="2f46c-113">The approximation tolerance to be used when preparing the given state.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="2f46c-114">coeficientes: [duplo](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="2f46c-114">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="2f46c-115">Matriz de até US $2 ^ n $ reais coeficientes.</span><span class="sxs-lookup"><span data-stu-id="2f46c-115">Array of up to $2^n$ real coefficients.</span></span> <span data-ttu-id="2f46c-116">O coeficiente $j $ th indexa o estado de número $ \ket{j} $ codificado em um formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="2f46c-116">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="2f46c-117">qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="2f46c-117">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="2f46c-118">Qubit registra os Estados de número de codificação no formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="2f46c-118">Qubit register encoding number states in little-endian format.</span></span> <span data-ttu-id="2f46c-119">Isso deve ser inicializado no estado de base computacional $ \ket{0...0} $.</span><span class="sxs-lookup"><span data-stu-id="2f46c-119">This is expected to be initialized in the computational basis state $\ket{0...0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2f46c-120">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2f46c-120">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="2f46c-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f46c-121">Remarks</span></span>

<span data-ttu-id="2f46c-122">Coeficientes de entrada negativas $r _j < $0 serão tratados como se positivo com o valor $ | r_j | $.</span><span class="sxs-lookup"><span data-stu-id="2f46c-122">Negative input coefficients $r_j < 0$ will be treated as though positive with value $|r_j|$.</span></span> <span data-ttu-id="2f46c-123">`coefficients` será preenchido com os elementos $ (r_j, t_j) = (0,0, 0,0) $ se menos de $2 ^ n $ forem especificados.</span><span class="sxs-lookup"><span data-stu-id="2f46c-123">`coefficients` will be padded with elements $(r_j, t_j) = (0.0, 0.0)$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="2f46c-124">Referências</span><span class="sxs-lookup"><span data-stu-id="2f46c-124">References</span></span>

- <span data-ttu-id="2f46c-125">Síntese de circuitos lógicos Quantum Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="2f46c-125">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>