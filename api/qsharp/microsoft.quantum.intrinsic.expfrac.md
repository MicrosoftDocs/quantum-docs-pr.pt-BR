---
uid: Microsoft.Quantum.Intrinsic.ExpFrac
title: Operação ExpFrac
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: ExpFrac
qsharp.summary: >-
  Applies the exponential of a multi-qubit Pauli operator with an argument given by a dyadic fraction.

  \begin{align} e^{i \pi k [P_0 \otimes P_1 \cdots P_{N-1}] / 2^n}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.
ms.openlocfilehash: d11912a272387b087098f59e7ac071534b01c054
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693339"
---
# <a name="expfrac-operation"></a><span data-ttu-id="39751-102">Operação ExpFrac</span><span class="sxs-lookup"><span data-stu-id="39751-102">ExpFrac operation</span></span>

<span data-ttu-id="39751-103">Namespace: [Microsoft. Quantum. intrínseco](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="39751-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="39751-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="39751-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="39751-105">Aplica o exponencial de um operador qubit Pauli com um argumento fornecido por uma fração dyadic.</span><span class="sxs-lookup"><span data-stu-id="39751-105">Applies the exponential of a multi-qubit Pauli operator with an argument given by a dyadic fraction.</span></span>

<span data-ttu-id="39751-106">\begin{align} e ^ {i \pi k [P_0 \otimes P_1 \cdots P_ {N-1}]/2 ^ N}, \end{align} em que $P _i $ é o elemento $i $ th de `paulis` e onde $N = $ `Length(paulis)` .</span><span class="sxs-lookup"><span data-stu-id="39751-106">\begin{align} e^{i \pi k [P_0 \otimes P_1 \cdots P_{N-1}] / 2^n}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.</span></span>

```qsharp
operation ExpFrac (paulis : Pauli[], numerator : Int, power : Int, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="39751-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="39751-107">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="39751-108">Paulis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="39751-108">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="39751-109">Matriz de valores de Pauli de qubit único que indicam os fatores de produto tensor em cada qubit.</span><span class="sxs-lookup"><span data-stu-id="39751-109">Array of single-qubit Pauli values indicating the tensor product factors on each qubit.</span></span>


### <a name="numerator--int"></a><span data-ttu-id="39751-110">numerador: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="39751-110">numerator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="39751-111">O numerador ($k $) na representação de fração dyadic do ângulo pelo qual o registro qubit deve ser girado.</span><span class="sxs-lookup"><span data-stu-id="39751-111">Numerator ($k$) in the dyadic fraction representation of the angle by which the qubit register is to be rotated.</span></span>


### <a name="power--int"></a><span data-ttu-id="39751-112">potência: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="39751-112">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="39751-113">Potência de dois ($n $) especificando o denominador do ângulo pelo qual o registro de qubit deve ser girado.</span><span class="sxs-lookup"><span data-stu-id="39751-113">Power of two ($n$) specifying the denominator of the angle by which the qubit register is to be rotated.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="39751-114">qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="39751-114">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="39751-115">Registre-se para aplicar a rotação fornecida ao.</span><span class="sxs-lookup"><span data-stu-id="39751-115">Register to apply the given rotation to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="39751-116">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="39751-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

