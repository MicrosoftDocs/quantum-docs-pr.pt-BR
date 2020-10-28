---
uid: Microsoft.Quantum.Canon.ApproximatelyApplyDiagonalUnitary
title: Operação ApproximatelyApplyDiagonalUnitary
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApproximatelyApplyDiagonalUnitary
qsharp.summary: Applies an array of complex phases to numeric basis states of a register of qubits, truncating small rotation angles according to a given tolerance.
ms.openlocfilehash: 9d9b1ced320b142aef2a2cd8f3335f855d37048f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694101"
---
# <a name="approximatelyapplydiagonalunitary-operation"></a><span data-ttu-id="a19e7-102">Operação ApproximatelyApplyDiagonalUnitary</span><span class="sxs-lookup"><span data-stu-id="a19e7-102">ApproximatelyApplyDiagonalUnitary operation</span></span>

<span data-ttu-id="a19e7-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a19e7-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a19e7-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a19e7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a19e7-105">Aplica uma matriz de fases complexas a Estados de base numéricos de um registro de qubits, truncando ângulos de rotação pequenos de acordo com uma determinada tolerância.</span><span class="sxs-lookup"><span data-stu-id="a19e7-105">Applies an array of complex phases to numeric basis states of a register of qubits, truncating small rotation angles according to a given tolerance.</span></span>

```qsharp
operation ApproximatelyApplyDiagonalUnitary (tolerance : Double, coefficients : Double[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="a19e7-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="a19e7-106">Description</span></span>

<span data-ttu-id="a19e7-107">Esta operação implementa um unitário diagonal que aplica uma fase complexa $e ^ {i \ theta_j} $ no estado do número do $n $-qubit $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="a19e7-107">This operation implements a diagonal unitary that applies a complex phase $e^{i \theta_j}$ on the $n$-qubit number state $\ket{j}$.</span></span>
<span data-ttu-id="a19e7-108">Em particular, essa operação pode ser representada pelo unitário</span><span class="sxs-lookup"><span data-stu-id="a19e7-108">In particular, this operation can be represented by the unitary</span></span>

<span data-ttu-id="a19e7-109">$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} e ^ {i \ theta_j} \ket{j}\bra{j}.</span><span class="sxs-lookup"><span data-stu-id="a19e7-109">$$ \begin{align} U = \sum^{2^n-1}_{j=0}e^{i\theta_j}\ket{j}\bra{j}.</span></span>
<span data-ttu-id="a19e7-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="a19e7-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="a19e7-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="a19e7-111">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="a19e7-112">tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="a19e7-112">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="a19e7-113">Uma tolerância abaixo que pequenos coeficientes são truncados.</span><span class="sxs-lookup"><span data-stu-id="a19e7-113">A tolerance below which small coefficients are truncated.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="a19e7-114">coeficientes: [duplo](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="a19e7-114">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="a19e7-115">Matriz de até $2 ^ n $ coeficientes $ \ theta_j $.</span><span class="sxs-lookup"><span data-stu-id="a19e7-115">Array of up to $2^n$ coefficients $\theta_j$.</span></span> <span data-ttu-id="a19e7-116">O coeficiente $j $ th indexa o estado de número $ \ket{j} $ codificado em um formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="a19e7-116">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="a19e7-117">qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="a19e7-117">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="a19e7-118">$n o registro de controle $-qubit que codifica Estados de número $ \ket{j} $ no formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="a19e7-118">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a19e7-119">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a19e7-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="a19e7-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="a19e7-120">Remarks</span></span>

<span data-ttu-id="a19e7-121">`coefficients` será preenchido com os elementos $ \ theta_j = $0 se menos de $2 ^ n $ forem especificados.</span><span class="sxs-lookup"><span data-stu-id="a19e7-121">`coefficients` will be padded with elements $\theta_j = 0.0$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="a19e7-122">Referências</span><span class="sxs-lookup"><span data-stu-id="a19e7-122">References</span></span>

- <span data-ttu-id="a19e7-123">Síntese de circuitos lógicos Quantum Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="a19e7-123">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="a19e7-124">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="a19e7-124">See Also</span></span>

- [<span data-ttu-id="a19e7-125">Microsoft. Quantum. Canon. ApplyDiagonalUnitary</span><span class="sxs-lookup"><span data-stu-id="a19e7-125">Microsoft.Quantum.Canon.ApplyDiagonalUnitary</span></span>](xref:Microsoft.Quantum.Canon.ApplyDiagonalUnitary)