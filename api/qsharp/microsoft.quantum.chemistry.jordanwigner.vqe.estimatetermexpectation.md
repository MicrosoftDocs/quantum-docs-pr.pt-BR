---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateTermExpectation
title: Operação EstimateTermExpectation
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateTermExpectation
qsharp.summary: Computes the energy associated to a given Jordan-Wigner Hamiltonian term
ms.openlocfilehash: ef689c55f966e63a2ab8bcdccf99d9cb5e6d3a4d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693659"
---
# <a name="estimatetermexpectation-operation"></a><span data-ttu-id="ab5b5-102">Operação EstimateTermExpectation</span><span class="sxs-lookup"><span data-stu-id="ab5b5-102">EstimateTermExpectation operation</span></span>

<span data-ttu-id="ab5b5-103">Namespace: [Microsoft. Quantum. química. JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="ab5b5-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="ab5b5-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ab5b5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ab5b5-105">Computa a energia associada a um determinado Jordan-Wigner termo Hamiltonian</span><span class="sxs-lookup"><span data-stu-id="ab5b5-105">Computes the energy associated to a given Jordan-Wigner Hamiltonian term</span></span>

```qsharp
operation EstimateTermExpectation (inputStateUnitary : (Qubit[] => Unit is Adj), ops : Pauli[][], coeffs : Double[], nQubits : Int, nSamples : Int) : Double
```


## <a name="description"></a><span data-ttu-id="ab5b5-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="ab5b5-106">Description</span></span>

<span data-ttu-id="ab5b5-107">Esta operação estima o valor de expectativa associado a cada operador de medida e o multiplica pelo coeficiente correspondente, usando a amostragem.</span><span class="sxs-lookup"><span data-stu-id="ab5b5-107">This operation estimates the expectation value associated to each measurement operator and multiplies it by the corresponding coefficient, using sampling.</span></span>
<span data-ttu-id="ab5b5-108">Os resultados são agregados em uma variável que contém a energia do termo de Jordan-Wigner.</span><span class="sxs-lookup"><span data-stu-id="ab5b5-108">The results are aggregated into a variable containing the energy of the Jordan-Wigner term.</span></span>

## <a name="input"></a><span data-ttu-id="ab5b5-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="ab5b5-109">Input</span></span>

### <a name="inputstateunitary--qubit--unit-adj"></a><span data-ttu-id="ab5b5-110">inputStateUnitary: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => adj da [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ab5b5-110">inputStateUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="ab5b5-111">O unitário usado para preparação do estado.</span><span class="sxs-lookup"><span data-stu-id="ab5b5-111">The unitary used for state preparation.</span></span>


### <a name="ops--pauli"></a><span data-ttu-id="ab5b5-112">Ops: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="ab5b5-112">ops : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="ab5b5-113">Os operadores de medida do termo de Jordan-Wigner.</span><span class="sxs-lookup"><span data-stu-id="ab5b5-113">The measurement operators of the Jordan-Wigner term.</span></span>


### <a name="coeffs--double"></a><span data-ttu-id="ab5b5-114">coeffs: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="ab5b5-114">coeffs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="ab5b5-115">Os coeficientes do termo de Jordan-Wigner.</span><span class="sxs-lookup"><span data-stu-id="ab5b5-115">The coefficients of the Jordan-Wigner term.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="ab5b5-116">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ab5b5-116">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ab5b5-117">O número de qubits necessárias para simular o sistema molecular.</span><span class="sxs-lookup"><span data-stu-id="ab5b5-117">The number of qubits required to simulate the molecular system.</span></span>


### <a name="nsamples--int"></a><span data-ttu-id="ab5b5-118">nSamples: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ab5b5-118">nSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ab5b5-119">O número de amostras a serem usadas para a estimativa da expectativa de termo.</span><span class="sxs-lookup"><span data-stu-id="ab5b5-119">The number of samples to use for the estimation of the term expectation.</span></span>



## <a name="output--double"></a><span data-ttu-id="ab5b5-120">Saída: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ab5b5-120">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ab5b5-121">A energia associada ao termo de Jordan-Wigner.</span><span class="sxs-lookup"><span data-stu-id="ab5b5-121">The energy associated to the Jordan-Wigner term.</span></span>