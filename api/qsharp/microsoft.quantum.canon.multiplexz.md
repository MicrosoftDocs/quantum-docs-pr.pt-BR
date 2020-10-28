---
uid: Microsoft.Quantum.Canon.MultiplexZ
title: Operação MultiplexZ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexZ
qsharp.summary: Applies a Pauli Z rotation conditioned on an array of qubits.
ms.openlocfilehash: f7b1973e18ad396ebe892ad63ae47374a7cafbd5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693952"
---
# <a name="multiplexz-operation"></a><span data-ttu-id="7e1e4-102">Operação MultiplexZ</span><span class="sxs-lookup"><span data-stu-id="7e1e4-102">MultiplexZ operation</span></span>

<span data-ttu-id="7e1e4-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7e1e4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7e1e4-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7e1e4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7e1e4-105">Aplica uma rotação de Pauli Z condicional em uma matriz de qubits.</span><span class="sxs-lookup"><span data-stu-id="7e1e4-105">Applies a Pauli Z rotation conditioned on an array of qubits.</span></span>

```qsharp
operation MultiplexZ (coefficients : Double[], control : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="7e1e4-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="7e1e4-106">Description</span></span>

<span data-ttu-id="7e1e4-107">Isso aplica a operação unitário controlada de multiplicação que executa rotações por ângulo $ \ theta_j $ sobre o operador Pauli de qubit único $Z $ quando controlado pelo estado do número $n $-qubit $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="7e1e4-107">This applies the multiply controlled unitary operation that performs rotations by angle $\theta_j$ about single-qubit Pauli operator $Z$ when controlled by the $n$-qubit number state $\ket{j}$.</span></span>
<span data-ttu-id="7e1e4-108">Em particular, essa operação pode ser representada pelo unitário</span><span class="sxs-lookup"><span data-stu-id="7e1e4-108">In particular, this operation can be represented by the unitary</span></span>

<span data-ttu-id="7e1e4-109">$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j} \otimes e ^ {i Z \ theta_j}.</span><span class="sxs-lookup"><span data-stu-id="7e1e4-109">$$ \begin{align} U = \sum^{2^n-1}_{j=0} \ket{j}\bra{j} \otimes e^{i Z \theta_j}.</span></span>
<span data-ttu-id="7e1e4-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="7e1e4-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="7e1e4-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e1e4-111">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="7e1e4-112">coeficientes: [duplo](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="7e1e4-112">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="7e1e4-113">Matriz de até $2 ^ n $ coeficientes $ \ theta_j $.</span><span class="sxs-lookup"><span data-stu-id="7e1e4-113">Array of up to $2^n$ coefficients $\theta_j$.</span></span> <span data-ttu-id="7e1e4-114">O coeficiente $j $ th indexa o estado de número $ \ket{j} $ codificado em um formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="7e1e4-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="control--littleendian"></a><span data-ttu-id="7e1e4-115">controle: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="7e1e4-115">control : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="7e1e4-116">$n o registro de controle $-qubit que codifica Estados de número $ \ket{j} $ no formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="7e1e4-116">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="7e1e4-117">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="7e1e4-117">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="7e1e4-118">Registro de qubit único que é girado por $e ^ {i P \ theta_j} $.</span><span class="sxs-lookup"><span data-stu-id="7e1e4-118">Single qubit register that is rotated by $e^{i P \theta_j}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7e1e4-119">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7e1e4-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="7e1e4-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e1e4-120">Remarks</span></span>

<span data-ttu-id="7e1e4-121">`coefficients` será preenchido com os elementos $ \ theta_j = $0 se menos de $2 ^ n $ forem especificados.</span><span class="sxs-lookup"><span data-stu-id="7e1e4-121">`coefficients` will be padded with elements $\theta_j = 0.0$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="7e1e4-122">Referências</span><span class="sxs-lookup"><span data-stu-id="7e1e4-122">References</span></span>

- <span data-ttu-id="7e1e4-123">Síntese de circuitos lógicos Quantum Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="7e1e4-123">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="7e1e4-124">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="7e1e4-124">See Also</span></span>

- [<span data-ttu-id="7e1e4-125">Microsoft. Quantum. Canon. ApproximatelyMultiplexZ</span><span class="sxs-lookup"><span data-stu-id="7e1e4-125">Microsoft.Quantum.Canon.ApproximatelyMultiplexZ</span></span>](xref:Microsoft.Quantum.Canon.ApproximatelyMultiplexZ)