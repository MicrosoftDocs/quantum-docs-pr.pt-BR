---
uid: Microsoft.Quantum.Intrinsic.Measure
title: Operação de medida
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Measure
qsharp.summary: >-
  Performs a joint measurement of one or more qubits in the specified Pauli bases.

  The output result is given by the distribution: \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \frac12 \braket{ \psi \mid| \left( \boldone + P_0 \otimes P_1 \otimes \cdots \otimes P_{N-1} \right) \mid| \psi }, \end{align} where $P_i$ is the $i$th element of `bases`, and where $N = \texttt{Length}(\texttt{bases})$. That is, measurement returns a `Result` $d$ such that the eigenvalue of the observed measurement effect is $(-1)^d$.
ms.openlocfilehash: 56ddfbe5e63692e477ad75bde6b1b16269ed20c0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693334"
---
# <a name="measure-operation"></a><span data-ttu-id="9e013-102">Operação de medida</span><span class="sxs-lookup"><span data-stu-id="9e013-102">Measure operation</span></span>

<span data-ttu-id="9e013-103">Namespace: [Microsoft. Quantum. intrínseco](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="9e013-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="9e013-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9e013-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9e013-105">Executa uma medida conjunta de um ou mais qubits nas bases de Pauli especificadas.</span><span class="sxs-lookup"><span data-stu-id="9e013-105">Performs a joint measurement of one or more qubits in the specified Pauli bases.</span></span>

<span data-ttu-id="9e013-106">O resultado de saída é fornecido pela distribuição: \begin{align} \Pr (\texttt{Zero} | \ket{\psi}) = \frac12 \braket{\psi \mid | \left (\boldone + P_0 \otimes P_1 \otimes \cdots \otimes P_ {N-1} \right) \mid | \psi}, \end{align} em que $P _i $ é o elemento $i $ th de `bases` e onde $N = \texttt{Length} (\texttt{bases}) $.</span><span class="sxs-lookup"><span data-stu-id="9e013-106">The output result is given by the distribution: \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \frac12 \braket{ \psi \mid| \left( \boldone + P_0 \otimes P_1 \otimes \cdots \otimes P_{N-1} \right) \mid| \psi }, \end{align} where $P_i$ is the $i$th element of `bases`, and where $N = \texttt{Length}(\texttt{bases})$.</span></span>
<span data-ttu-id="9e013-107">Ou seja, a medida retorna um `Result` $d $ de modo que o eigenvalue do efeito de medição observado é $ (-1) ^ d $.</span><span class="sxs-lookup"><span data-stu-id="9e013-107">That is, measurement returns a `Result` $d$ such that the eigenvalue of the observed measurement effect is $(-1)^d$.</span></span>

```qsharp
operation Measure (bases : Pauli[], qubits : Qubit[]) : Result
```


## <a name="input"></a><span data-ttu-id="9e013-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="9e013-108">Input</span></span>

### <a name="bases--pauli"></a><span data-ttu-id="9e013-109">bases: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="9e013-109">bases : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="9e013-110">Matriz de valores de Pauli de qubit único que indicam os fatores de produto tensor em cada qubit.</span><span class="sxs-lookup"><span data-stu-id="9e013-110">Array of single-qubit Pauli values indicating the tensor product factors on each qubit.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="9e013-111">qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="9e013-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="9e013-112">Registro de qubits a ser medido.</span><span class="sxs-lookup"><span data-stu-id="9e013-112">Register of qubits to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="9e013-113">Saída: __inválida <Result>__</span><span class="sxs-lookup"><span data-stu-id="9e013-113">Output : __invalid<Result>__</span></span>

<span data-ttu-id="9e013-114">`Zero` Se o $ + $1 eigenvalue for observado e `One` se o eigenvalue $-$1 for observado.</span><span class="sxs-lookup"><span data-stu-id="9e013-114">`Zero` if the $+1$ eigenvalue is observed, and `One` if the $-1$ eigenvalue is observed.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e013-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e013-115">Remarks</span></span>

<span data-ttu-id="9e013-116">Se a matriz de base e a matriz qubit tiverem comprimentos diferentes, a operação falhará.</span><span class="sxs-lookup"><span data-stu-id="9e013-116">If the basis array and qubit array are different lengths, then the operation will fail.</span></span>