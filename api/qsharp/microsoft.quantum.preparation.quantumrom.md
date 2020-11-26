---
uid: Microsoft.Quantum.Preparation.QuantumROM
title: Função QuantumROM
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: QuantumROM
qsharp.summary: >-
  > [!WARNING]

  > QuantumROM has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PurifiedMixedState> instead.


  Uses the Quantum ROM technique to represent a given density matrix.

  Given a list of $N$ coefficients $\alpha_j$, this returns a unitary $U$ that uses the Quantum-ROM technique to prepare an approximation  $\tilde\rho\sum_{j=0}^{N-1}p_j\ket{j}\bra{j}$ of the purification of the density matrix $\rho=\sum_{j=0}^{N-1}\frac{|alpha_j|}{\sum_k |\alpha_k|}\ket{j}\bra{j}$. In this approximation, the error $\epsilon$ is such that $|p_j-\frac{|alpha_j|}{\sum_k |\alpha_k|}|\le \epsilon / N$ and $\|\tilde\rho - \rho\| \le \epsilon$. In other words, $$ \begin{align} U\ket{0}^{\lceil\log_2 N\rceil}\ket{0}^{m}=\sum_{j=0}^{N-1}\sqrt{p_j} \ket{j}\ket{\text{garbage}_j}. \end{align} $$
ms.openlocfilehash: 1ee805fb2ea02121daaab7fc3eb5dbbcb134b470
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229878"
---
# <a name="quantumrom-function"></a><span data-ttu-id="6311d-102">Função QuantumROM</span><span class="sxs-lookup"><span data-stu-id="6311d-102">QuantumROM function</span></span>

<span data-ttu-id="6311d-103">Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="6311d-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="6311d-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6311d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="6311d-105">QuantumROM foi preterido.</span><span class="sxs-lookup"><span data-stu-id="6311d-105">QuantumROM has been deprecated.</span></span> <span data-ttu-id="6311d-106">Use <xref:Microsoft.Quantum.Preparation.PurifiedMixedState> em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="6311d-106">Please use <xref:Microsoft.Quantum.Preparation.PurifiedMixedState> instead.</span></span>

<span data-ttu-id="6311d-107">Usa a técnica de ROM Quantum para representar uma determinada matriz de densidade.</span><span class="sxs-lookup"><span data-stu-id="6311d-107">Uses the Quantum ROM technique to represent a given density matrix.</span></span>

<span data-ttu-id="6311d-108">Dada uma lista de $N $ coeficientes $ \ alpha_j $, isso retorna um $U unitário que usa a técnica Quantum-ROM para preparar uma aproximação $ \tilde\rho\ sum_ {j = 0} ^ {N-1} p_j \ket{j}\bra{j} $ do Purification da matriz de densidade $ \rho = \ sum_ {j = 0} ^ {N-1} \frac{| alpha_j |} {\ sum_k | \ alpha_k |} \ket{j}\bra{j} $.</span><span class="sxs-lookup"><span data-stu-id="6311d-108">Given a list of $N$ coefficients $\alpha_j$, this returns a unitary $U$ that uses the Quantum-ROM technique to prepare an approximation  $\tilde\rho\sum_{j=0}^{N-1}p_j\ket{j}\bra{j}$ of the purification of the density matrix $\rho=\sum_{j=0}^{N-1}\frac{|alpha_j|}{\sum_k |\alpha_k|}\ket{j}\bra{j}$.</span></span> <span data-ttu-id="6311d-109">Nessa aproximação, o erro $ \epsilon $ é de que $ | p_j-\frac{| alpha_j |} {\ sum_k | \ alpha_k |} | \le \epsilon/N $ e $ \| \tilde\rho-\rho \| \le \epsilon $.</span><span class="sxs-lookup"><span data-stu-id="6311d-109">In this approximation, the error $\epsilon$ is such that $|p_j-\frac{|alpha_j|}{\sum_k |\alpha_k|}|\le \epsilon / N$ and $\|\tilde\rho - \rho\| \le \epsilon$.</span></span> <span data-ttu-id="6311d-110">Em outras palavras, $ $ \begin{align} U\ket {0} ^ {\lceil\ Log_2 N\rceil} \ ket {0} ^ {m} = \ sum_ {j = 0} ^ {N-1} \sqrt{p_j} \ket{j}\ket{\Text{Garbage} _J}.</span><span class="sxs-lookup"><span data-stu-id="6311d-110">In other words, $$ \begin{align} U\ket{0}^{\lceil\log_2 N\rceil}\ket{0}^{m}=\sum_{j=0}^{N-1}\sqrt{p_j} \ket{j}\ket{\text{garbage}_j}.</span></span>
<span data-ttu-id="6311d-111">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="6311d-111">\end{align} $$</span></span>

```qsharp
function QuantumROM (targetError : Double, coefficients : Double[]) : ((Int, (Int, Int)), Double, ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl))
```


## <a name="input"></a><span data-ttu-id="6311d-112">Entrada</span><span class="sxs-lookup"><span data-stu-id="6311d-112">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="6311d-113">targetError: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="6311d-113">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="6311d-114">O erro de destino $ \epsilon $.</span><span class="sxs-lookup"><span data-stu-id="6311d-114">The target error $\epsilon$.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="6311d-115">coeficientes: [duplo](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="6311d-115">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="6311d-116">Matriz de $N $ coeficientes especificando a probabilidade de Estados de base.</span><span class="sxs-lookup"><span data-stu-id="6311d-116">Array of $N$ coefficients specifying the probability of basis states.</span></span>
<span data-ttu-id="6311d-117">Números negativos $-\ alpha_j $ serão tratados como $ | \ alpha_j | $.</span><span class="sxs-lookup"><span data-stu-id="6311d-117">Negative numbers $-\alpha_j$ will be treated as positive $|\alpha_j|$.</span></span>



## <a name="output--intintintdoublelittleendianqubit--unit--is-adj--ctl"></a><span data-ttu-id="6311d-118">Saída: (([int](xref:microsoft.quantum.lang-ref.int), ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))),[Double](xref:microsoft.quantum.lang-ref.double), ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL)</span><span class="sxs-lookup"><span data-stu-id="6311d-118">Output : (([Int](xref:microsoft.quantum.lang-ref.int),([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))),[Double](xref:microsoft.quantum.lang-ref.double),([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl)</span></span>

## <a name="first-parameter"></a><span data-ttu-id="6311d-119">Primeiro parâmetro</span><span class="sxs-lookup"><span data-stu-id="6311d-119">First parameter</span></span>

<span data-ttu-id="6311d-120">Uma tupla `(x,(y,z))` em que `x = y + z` é o número total de qubits alocadas, `y` é o número de qubits para o `LittleEndian` registro e `z` é o número de qubits de lixo.</span><span class="sxs-lookup"><span data-stu-id="6311d-120">A tuple `(x,(y,z))` where `x = y + z` is the total number of qubits allocated, `y` is the number of qubits for the `LittleEndian` register, and `z` is the Number of garbage qubits.</span></span>

## <a name="second-parameter"></a><span data-ttu-id="6311d-121">Segundo parâmetro</span><span class="sxs-lookup"><span data-stu-id="6311d-121">Second parameter</span></span>

<span data-ttu-id="6311d-122">A norma One-Activity $ \ sum_j | \ alpha_j | $ da matriz de coeficiente.</span><span class="sxs-lookup"><span data-stu-id="6311d-122">The one-norm $\sum_j |\alpha_j|$ of the coefficient array.</span></span>

## <a name="third-parameter"></a><span data-ttu-id="6311d-123">Terceiro parâmetro</span><span class="sxs-lookup"><span data-stu-id="6311d-123">Third parameter</span></span>

<span data-ttu-id="6311d-124">O unitário $U $.</span><span class="sxs-lookup"><span data-stu-id="6311d-124">The unitary $U$.</span></span>

## <a name="references"></a><span data-ttu-id="6311d-125">Referências</span><span class="sxs-lookup"><span data-stu-id="6311d-125">References</span></span>

- <span data-ttu-id="6311d-126">Codificação eletrônica de Spectra em circuitos Quantum com complexidade T linear Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru fosco, Austin Fowler, Hartmut Neven https://arxiv.org/abs/1805.03662</span><span class="sxs-lookup"><span data-stu-id="6311d-126">Encoding Electronic Spectra in Quantum Circuits with Linear T Complexity Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru Paler, Austin Fowler, Hartmut Neven https://arxiv.org/abs/1805.03662</span></span>