---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateTermExpectation
title: Operação EstimateTermExpectation
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateTermExpectation
qsharp.summary: Computes the energy associated to a given Jordan-Wigner Hamiltonian term
ms.openlocfilehash: 7df4c1ea859140a669698434c6f8a786ea3bc2ea
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98835662"
---
# <a name="estimatetermexpectation-operation"></a><span data-ttu-id="16865-102">Operação EstimateTermExpectation</span><span class="sxs-lookup"><span data-stu-id="16865-102">EstimateTermExpectation operation</span></span>

<span data-ttu-id="16865-103">Namespace: [Microsoft. Quantum. química. JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="16865-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="16865-104">Pacote: [Microsoft. Quantum. química](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="16865-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="16865-105">Computa a energia associada a um determinado Jordan-Wigner termo Hamiltonian</span><span class="sxs-lookup"><span data-stu-id="16865-105">Computes the energy associated to a given Jordan-Wigner Hamiltonian term</span></span>

```qsharp
operation EstimateTermExpectation (inputStateUnitary : (Qubit[] => Unit is Adj), ops : Pauli[][], coeffs : Double[], nQubits : Int, nSamples : Int) : Double
```


## <a name="description"></a><span data-ttu-id="16865-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="16865-106">Description</span></span>

<span data-ttu-id="16865-107">Esta operação estima o valor de expectativa associado a cada operador de medida e o multiplica pelo coeficiente correspondente, usando a amostragem.</span><span class="sxs-lookup"><span data-stu-id="16865-107">This operation estimates the expectation value associated to each measurement operator and multiplies it by the corresponding coefficient, using sampling.</span></span>
<span data-ttu-id="16865-108">Os resultados são agregados em uma variável que contém a energia do termo de Jordan-Wigner.</span><span class="sxs-lookup"><span data-stu-id="16865-108">The results are aggregated into a variable containing the energy of the Jordan-Wigner term.</span></span>

## <a name="input"></a><span data-ttu-id="16865-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="16865-109">Input</span></span>

### <a name="inputstateunitary--qubit--unit--is-adj"></a><span data-ttu-id="16865-110">inputStateUnitary: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj</span><span class="sxs-lookup"><span data-stu-id="16865-110">inputStateUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="16865-111">O unitário usado para preparação do estado.</span><span class="sxs-lookup"><span data-stu-id="16865-111">The unitary used for state preparation.</span></span>


### <a name="ops--pauli"></a><span data-ttu-id="16865-112">Ops: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="16865-112">ops : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="16865-113">Os operadores de medida do termo de Jordan-Wigner.</span><span class="sxs-lookup"><span data-stu-id="16865-113">The measurement operators of the Jordan-Wigner term.</span></span>


### <a name="coeffs--double"></a><span data-ttu-id="16865-114">coeffs: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="16865-114">coeffs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="16865-115">Os coeficientes do termo de Jordan-Wigner.</span><span class="sxs-lookup"><span data-stu-id="16865-115">The coefficients of the Jordan-Wigner term.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="16865-116">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="16865-116">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="16865-117">O número de qubits necessárias para simular o sistema molecular.</span><span class="sxs-lookup"><span data-stu-id="16865-117">The number of qubits required to simulate the molecular system.</span></span>


### <a name="nsamples--int"></a><span data-ttu-id="16865-118">nSamples: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="16865-118">nSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="16865-119">O número de amostras a serem usadas para a estimativa da expectativa de termo.</span><span class="sxs-lookup"><span data-stu-id="16865-119">The number of samples to use for the estimation of the term expectation.</span></span>



## <a name="output--double"></a><span data-ttu-id="16865-120">Saída: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="16865-120">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="16865-121">A energia associada ao termo de Jordan-Wigner.</span><span class="sxs-lookup"><span data-stu-id="16865-121">The energy associated to the Jordan-Wigner term.</span></span>