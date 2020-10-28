---
uid: Microsoft.Quantum.Canon.MultiplexPauli
title: Operação MultiplexPauli
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexPauli
qsharp.summary: Applies a Pauli rotation conditioned on an array of qubits.
ms.openlocfilehash: 0714e796c1e5ad097814bcf507f49f59a844e9ff
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693953"
---
# <a name="multiplexpauli-operation"></a><span data-ttu-id="29c8f-102">Operação MultiplexPauli</span><span class="sxs-lookup"><span data-stu-id="29c8f-102">MultiplexPauli operation</span></span>

<span data-ttu-id="29c8f-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="29c8f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="29c8f-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="29c8f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="29c8f-105">Aplica uma rotação Pauli condição em uma matriz de qubits.</span><span class="sxs-lookup"><span data-stu-id="29c8f-105">Applies a Pauli rotation conditioned on an array of qubits.</span></span>

```qsharp
operation MultiplexPauli (coefficients : Double[], pauli : Pauli, control : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="29c8f-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="29c8f-106">Description</span></span>

<span data-ttu-id="29c8f-107">Isso aplica uma operação unitário controlada com controle de multiplicação que executa rotações por meio do ângulo $ \ theta_j $ sobre o operador Pauli de qubit único $P $ quando controlado pelo estado do número $n $-qubit $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="29c8f-107">This applies a multiply controlled unitary operation that performs rotations by angle $\theta_j$ about single-qubit Pauli operator $P$ when controlled by the $n$-qubit number state $\ket{j}$.</span></span>
<span data-ttu-id="29c8f-108">Em particular, a ação dessa operação é representada pelo unitário</span><span class="sxs-lookup"><span data-stu-id="29c8f-108">In particular, the action of this operation is represented by the unitary</span></span>

<span data-ttu-id="29c8f-109">$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j} \otimes e ^ {i P \ theta_j}.</span><span class="sxs-lookup"><span data-stu-id="29c8f-109">$$ \begin{align} U = \sum^{2^n - 1}_{j=0} \ket{j}\bra{j} \otimes e^{i P \theta_j}.</span></span>
<span data-ttu-id="29c8f-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="29c8f-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="29c8f-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="29c8f-111">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="29c8f-112">coeficientes: [duplo](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="29c8f-112">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="29c8f-113">Matriz de até $2 ^ n $ coeficientes $ \ theta_j $.</span><span class="sxs-lookup"><span data-stu-id="29c8f-113">Array of up to $2^n$ coefficients $\theta_j$.</span></span> <span data-ttu-id="29c8f-114">O coeficiente $j $ th indexa o estado de número $ \ket{j} $ codificado em um formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="29c8f-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="pauli--pauli"></a><span data-ttu-id="29c8f-115">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="29c8f-115">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="29c8f-116">Operador Pauli $P $ que determina o eixo de rotação.</span><span class="sxs-lookup"><span data-stu-id="29c8f-116">Pauli operator $P$ that determines axis of rotation.</span></span>


### <a name="control--littleendian"></a><span data-ttu-id="29c8f-117">controle: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="29c8f-117">control : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="29c8f-118">$n o registro de controle $-qubit que codifica Estados de número $ \ket{j} $ no formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="29c8f-118">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="29c8f-119">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="29c8f-119">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="29c8f-120">Registro de qubit único que é girado por $e ^ {i P \ theta_j} $.</span><span class="sxs-lookup"><span data-stu-id="29c8f-120">Single qubit register that is rotated by $e^{i P \theta_j}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="29c8f-121">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="29c8f-121">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="29c8f-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="29c8f-122">Remarks</span></span>

<span data-ttu-id="29c8f-123">`coefficients` será preenchido com os elementos $ \ theta_j = $0 se menos de $2 ^ n $ forem especificados.</span><span class="sxs-lookup"><span data-stu-id="29c8f-123">`coefficients` will be padded with elements $\theta_j = 0.0$ if fewer than $2^n$ are specified.</span></span>

## <a name="see-also"></a><span data-ttu-id="29c8f-124">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="29c8f-124">See Also</span></span>

- [<span data-ttu-id="29c8f-125">Microsoft. Quantum. Canon. ApproximatelyMultiplexPauli</span><span class="sxs-lookup"><span data-stu-id="29c8f-125">Microsoft.Quantum.Canon.ApproximatelyMultiplexPauli</span></span>](xref:Microsoft.Quantum.Canon.ApproximatelyMultiplexPauli)