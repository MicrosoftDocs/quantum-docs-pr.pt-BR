---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateTermExpectation
title: Operação EstimateTermExpectation
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateTermExpectation
qsharp.summary: Computes the energy associated to a given Jordan-Wigner Hamiltonian term
ms.openlocfilehash: 3f0ff5037b1424abb6fb318bd49ffd89f545822d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224642"
---
# <a name="estimatetermexpectation-operation"></a><span data-ttu-id="195d3-102">Operação EstimateTermExpectation</span><span class="sxs-lookup"><span data-stu-id="195d3-102">EstimateTermExpectation operation</span></span>

<span data-ttu-id="195d3-103">Namespace: [Microsoft. Quantum. química. JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="195d3-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="195d3-104">Pacote: [Microsoft. Quantum. química](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="195d3-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="195d3-105">Computa a energia associada a um determinado Jordan-Wigner termo Hamiltonian</span><span class="sxs-lookup"><span data-stu-id="195d3-105">Computes the energy associated to a given Jordan-Wigner Hamiltonian term</span></span>

```qsharp
operation EstimateTermExpectation (inputStateUnitary : (Qubit[] => Unit is Adj), ops : Pauli[][], coeffs : Double[], nQubits : Int, nSamples : Int) : Double
```


## <a name="description"></a><span data-ttu-id="195d3-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="195d3-106">Description</span></span>

<span data-ttu-id="195d3-107">Esta operação estima o valor de expectativa associado a cada operador de medida e o multiplica pelo coeficiente correspondente, usando a amostragem.</span><span class="sxs-lookup"><span data-stu-id="195d3-107">This operation estimates the expectation value associated to each measurement operator and multiplies it by the corresponding coefficient, using sampling.</span></span>
<span data-ttu-id="195d3-108">Os resultados são agregados em uma variável que contém a energia do termo de Jordan-Wigner.</span><span class="sxs-lookup"><span data-stu-id="195d3-108">The results are aggregated into a variable containing the energy of the Jordan-Wigner term.</span></span>

## <a name="input"></a><span data-ttu-id="195d3-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="195d3-109">Input</span></span>

### <a name="inputstateunitary--qubit--unit--is-adj"></a><span data-ttu-id="195d3-110">inputStateUnitary: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj</span><span class="sxs-lookup"><span data-stu-id="195d3-110">inputStateUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="195d3-111">O unitário usado para preparação do estado.</span><span class="sxs-lookup"><span data-stu-id="195d3-111">The unitary used for state preparation.</span></span>


### <a name="ops--pauli"></a><span data-ttu-id="195d3-112">Ops: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="195d3-112">ops : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="195d3-113">Os operadores de medida do termo de Jordan-Wigner.</span><span class="sxs-lookup"><span data-stu-id="195d3-113">The measurement operators of the Jordan-Wigner term.</span></span>


### <a name="coeffs--double"></a><span data-ttu-id="195d3-114">coeffs: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="195d3-114">coeffs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="195d3-115">Os coeficientes do termo de Jordan-Wigner.</span><span class="sxs-lookup"><span data-stu-id="195d3-115">The coefficients of the Jordan-Wigner term.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="195d3-116">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="195d3-116">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="195d3-117">O número de qubits necessárias para simular o sistema molecular.</span><span class="sxs-lookup"><span data-stu-id="195d3-117">The number of qubits required to simulate the molecular system.</span></span>


### <a name="nsamples--int"></a><span data-ttu-id="195d3-118">nSamples: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="195d3-118">nSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="195d3-119">O número de amostras a serem usadas para a estimativa da expectativa de termo.</span><span class="sxs-lookup"><span data-stu-id="195d3-119">The number of samples to use for the estimation of the term expectation.</span></span>



## <a name="output--double"></a><span data-ttu-id="195d3-120">Saída: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="195d3-120">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="195d3-121">A energia associada ao termo de Jordan-Wigner.</span><span class="sxs-lookup"><span data-stu-id="195d3-121">The energy associated to the Jordan-Wigner term.</span></span>