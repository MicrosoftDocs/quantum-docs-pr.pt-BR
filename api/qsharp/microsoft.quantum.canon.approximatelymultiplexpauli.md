---
uid: Microsoft.Quantum.Canon.ApproximatelyMultiplexPauli
title: Operação ApproximatelyMultiplexPauli
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApproximatelyMultiplexPauli
qsharp.summary: Applies a Pauli rotation conditioned on an array of qubits, truncating small rotation angles according to a given tolerance.
ms.openlocfilehash: 8024df4608f14408bfcd46139e72454ff44b116f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207744"
---
# <a name="approximatelymultiplexpauli-operation"></a><span data-ttu-id="95713-102">Operação ApproximatelyMultiplexPauli</span><span class="sxs-lookup"><span data-stu-id="95713-102">ApproximatelyMultiplexPauli operation</span></span>

<span data-ttu-id="95713-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="95713-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="95713-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="95713-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="95713-105">Aplica uma rotação Pauli condição em uma matriz de qubits, truncando pequenos ângulos de rotação de acordo com uma determinada tolerância.</span><span class="sxs-lookup"><span data-stu-id="95713-105">Applies a Pauli rotation conditioned on an array of qubits, truncating small rotation angles according to a given tolerance.</span></span>

```qsharp
operation ApproximatelyMultiplexPauli (tolerance : Double, coefficients : Double[], pauli : Pauli, control : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="95713-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="95713-106">Description</span></span>

<span data-ttu-id="95713-107">Isso aplica uma operação unitário controlada com controle de multiplicação que executa rotações por meio do ângulo $ \ theta_j $ sobre o operador Pauli de qubit único $P $ quando controlado pelo estado do número $n $-qubit $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="95713-107">This applies a multiply controlled unitary operation that performs rotations by angle $\theta_j$ about single-qubit Pauli operator $P$ when controlled by the $n$-qubit number state $\ket{j}$.</span></span>
<span data-ttu-id="95713-108">Em particular, a ação dessa operação é representada pelo unitário</span><span class="sxs-lookup"><span data-stu-id="95713-108">In particular, the action of this operation is represented by the unitary</span></span>

<span data-ttu-id="95713-109">$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j} \otimes e ^ {i P \ theta_j}.</span><span class="sxs-lookup"><span data-stu-id="95713-109">$$ \begin{align} U = \sum^{2^n - 1}_{j=0} \ket{j}\bra{j} \otimes e^{i P \theta_j}.</span></span>
<span data-ttu-id="95713-110">\end{align}</span><span class="sxs-lookup"><span data-stu-id="95713-110">\end{align}</span></span>

##

## <a name="input"></a><span data-ttu-id="95713-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="95713-111">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="95713-112">tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="95713-112">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="95713-113">Uma tolerância abaixo que pequenos coeficientes são truncados.</span><span class="sxs-lookup"><span data-stu-id="95713-113">A tolerance below which small coefficients are truncated.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="95713-114">coeficientes: [duplo](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="95713-114">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="95713-115">Matriz de até $2 ^ n $ coeficientes $ \ theta_j $.</span><span class="sxs-lookup"><span data-stu-id="95713-115">Array of up to $2^n$ coefficients $\theta_j$.</span></span> <span data-ttu-id="95713-116">O coeficiente $j $ th indexa o estado de número $ \ket{j} $ codificado em um formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="95713-116">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="pauli--pauli"></a><span data-ttu-id="95713-117">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="95713-117">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="95713-118">Operador Pauli $P $ que determina o eixo de rotação.</span><span class="sxs-lookup"><span data-stu-id="95713-118">Pauli operator $P$ that determines axis of rotation.</span></span>


### <a name="control--littleendian"></a><span data-ttu-id="95713-119">controle: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="95713-119">control : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="95713-120">$n o registro de controle $-qubit que codifica Estados de número $ \ket{j} $ no formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="95713-120">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="95713-121">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="95713-121">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="95713-122">Registro de qubit único que é girado por $e ^ {i P \ theta_j} $.</span><span class="sxs-lookup"><span data-stu-id="95713-122">Single qubit register that is rotated by $e^{i P \theta_j}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="95713-123">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="95713-123">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="95713-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="95713-124">Remarks</span></span>

<span data-ttu-id="95713-125">`coefficients` será preenchido com os elementos $ \ theta_j = $0 se menos de $2 ^ n $ forem especificados.</span><span class="sxs-lookup"><span data-stu-id="95713-125">`coefficients` will be padded with elements $\theta_j = 0.0$ if fewer than $2^n$ are specified.</span></span>

## <a name="see-also"></a><span data-ttu-id="95713-126">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="95713-126">See Also</span></span>

- [<span data-ttu-id="95713-127">Microsoft. Quantum. Canon. MultiplexPauli</span><span class="sxs-lookup"><span data-stu-id="95713-127">Microsoft.Quantum.Canon.MultiplexPauli</span></span>](xref:Microsoft.Quantum.Canon.MultiplexPauli)