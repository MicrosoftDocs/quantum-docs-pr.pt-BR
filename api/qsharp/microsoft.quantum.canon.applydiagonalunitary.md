---
uid: Microsoft.Quantum.Canon.ApplyDiagonalUnitary
title: Operação ApplyDiagonalUnitary
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyDiagonalUnitary
qsharp.summary: Applies an array of complex phases to numeric basis states of a register of qubits.
ms.openlocfilehash: 14ab8d7beddda26594967225934d472d52bac9eb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841898"
---
# <a name="applydiagonalunitary-operation"></a><span data-ttu-id="08855-102">Operação ApplyDiagonalUnitary</span><span class="sxs-lookup"><span data-stu-id="08855-102">ApplyDiagonalUnitary operation</span></span>

<span data-ttu-id="08855-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="08855-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="08855-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="08855-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="08855-105">Aplica uma matriz de fases complexas a Estados de base numéricos de um registro de qubits.</span><span class="sxs-lookup"><span data-stu-id="08855-105">Applies an array of complex phases to numeric basis states of a register of qubits.</span></span>

```qsharp
operation ApplyDiagonalUnitary (coefficients : Double[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="08855-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="08855-106">Description</span></span>

<span data-ttu-id="08855-107">Esta operação implementa um unitário diagonal que aplica uma fase complexa $e ^ {i \ theta_j} $ no estado do número do $n $-qubit $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="08855-107">This operation implements a diagonal unitary that applies a complex phase $e^{i \theta_j}$ on the $n$-qubit number state $\ket{j}$.</span></span>
<span data-ttu-id="08855-108">Em particular, essa operação pode ser representada pelo unitário</span><span class="sxs-lookup"><span data-stu-id="08855-108">In particular, this operation can be represented by the unitary</span></span>

<span data-ttu-id="08855-109">$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} e ^ {i \ theta_j} \ket{j}\bra{j}.</span><span class="sxs-lookup"><span data-stu-id="08855-109">$$ \begin{align} U = \sum^{2^n-1}_{j=0}e^{i\theta_j}\ket{j}\bra{j}.</span></span>
<span data-ttu-id="08855-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="08855-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="08855-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="08855-111">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="08855-112">coeficientes: [duplo](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="08855-112">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="08855-113">Matriz de até $2 ^ n $ coeficientes $ \ theta_j $.</span><span class="sxs-lookup"><span data-stu-id="08855-113">Array of up to $2^n$ coefficients $\theta_j$.</span></span> <span data-ttu-id="08855-114">O coeficiente $j $ th indexa o estado de número $ \ket{j} $ codificado em um formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="08855-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="08855-115">qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="08855-115">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="08855-116">$n o registro de controle $-qubit que codifica Estados de número $ \ket{j} $ no formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="08855-116">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>



## <a name="output--unit"></a><span data-ttu-id="08855-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="08855-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="08855-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="08855-118">Remarks</span></span>

<span data-ttu-id="08855-119">`coefficients` será preenchido com os elementos $ \ theta_j = $0 se menos de $2 ^ n $ forem especificados.</span><span class="sxs-lookup"><span data-stu-id="08855-119">`coefficients` will be padded with elements $\theta_j = 0.0$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="08855-120">Referências</span><span class="sxs-lookup"><span data-stu-id="08855-120">References</span></span>

- <span data-ttu-id="08855-121">Síntese de circuitos lógicos Quantum Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="08855-121">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="08855-122">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="08855-122">See Also</span></span>

- [<span data-ttu-id="08855-123">Microsoft. Quantum. Canon. ApproximatelyApplyDiagonalUnitary</span><span class="sxs-lookup"><span data-stu-id="08855-123">Microsoft.Quantum.Canon.ApproximatelyApplyDiagonalUnitary</span></span>](xref:Microsoft.Quantum.Canon.ApproximatelyApplyDiagonalUnitary)