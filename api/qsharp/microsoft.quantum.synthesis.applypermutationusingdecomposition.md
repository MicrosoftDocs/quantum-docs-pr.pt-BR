---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition
title: Operação ApplyPermutationUsingDecomposition
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingDecomposition
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.
ms.openlocfilehash: 40b51807da155c57c3fa8d740eff28ceef0a0ffc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92697068"
---
# <a name="applypermutationusingdecomposition-operation"></a><span data-ttu-id="c2dd4-102">Operação ApplyPermutationUsingDecomposition</span><span class="sxs-lookup"><span data-stu-id="c2dd4-102">ApplyPermutationUsingDecomposition operation</span></span>

<span data-ttu-id="c2dd4-103">Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="c2dd4-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="c2dd4-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c2dd4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c2dd4-105">Permuta as amplitudes em um estado Quantum, considerando uma permuta usando a síntese baseada em decomposição.</span><span class="sxs-lookup"><span data-stu-id="c2dd4-105">Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.</span></span>

```qsharp
operation ApplyPermutationUsingDecomposition (perm : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="c2dd4-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2dd4-106">Description</span></span>

<span data-ttu-id="c2dd4-107">Esse procedimento implementa a abordagem de síntese baseada em decomposição.</span><span class="sxs-lookup"><span data-stu-id="c2dd4-107">This procedure implements the decomposition based synthesis approach.</span></span>  <span data-ttu-id="c2dd4-108">A entrada é uma permutação $ \pi $ sobre $2 ^ n $ Elements $ \{ 0, \dots, 2 ^ n-1 \} $, que representa uma função booliana $n $-Variable reversível.</span><span class="sxs-lookup"><span data-stu-id="c2dd4-108">The input is a permutation $\pi$ over $2^n$ elements $\{0, \dots, 2^n-1\}$, which represents an $n$-variable reversible Boolean function.</span></span>
<span data-ttu-id="c2dd4-109">O algoritmo executa iterativamente as seguintes etapas para cada índice variável $i $:</span><span class="sxs-lookup"><span data-stu-id="c2dd4-109">The algorithm iteratively performs the following steps for each variable index $i$:</span></span>

1. <span data-ttu-id="c2dd4-110">Compute $ ((\ pi_l, \ pi_r), \pi ') $ de forma que as imagens de $ \ pi_l $ e $ \ pi_r $ não alterem bits em seus elementos em índices diferentes de $i $ e imagens de $ \pi ' $ não alterar bit $i $ em seus elementos.</span><span class="sxs-lookup"><span data-stu-id="c2dd4-110">Compute $((\pi_l, \pi_r), \pi')$ such that the images of $\pi_l$ and $\pi_r$ do not change bits in their elements at indexes other than $i$ and images of $\pi'$ do not change bit $i$ in their elements.</span></span>
2. <span data-ttu-id="c2dd4-111">Defina $ \pi \leftarrow \pi ' $ ' e derive as tabelas da verdade de $ \ pi_l $ e $ \ pi_r $ com base em elementos que não são pontos fixos.</span><span class="sxs-lookup"><span data-stu-id="c2dd4-111">Set $\pi \leftarrow \pi'$, and derive truth tables from $\pi_l$ and $\pi_r$ based on elements that are not fixed-points.</span></span>

<span data-ttu-id="c2dd4-112">Depois de aplicar essas etapas para todos os índices de variáveis, a permutação restante $ \pi $ será a identidade e, com base nas tabelas e índices da verdade coletados, uma poderá aplicar as operações controladas de verdade @"microsoft.quantum.intrinsic.x" da tabela usando a @"microsoft.quantum.synthesis.applyxcontrolledontruthtable" operação.</span><span class="sxs-lookup"><span data-stu-id="c2dd4-112">After applying these steps for all variable indexes, the remaining permutation $\pi$ will be the identity, and based on the collected truth tables and indexes, one can apply truth-table controlled @"microsoft.quantum.intrinsic.x" operations using the @"microsoft.quantum.synthesis.applyxcontrolledontruthtable" operation.</span></span>

<span data-ttu-id="c2dd4-113">A ordem da variável é $0, \dots, n-$1.</span><span class="sxs-lookup"><span data-stu-id="c2dd4-113">The variable order is $0, \dots, n - 1$.</span></span>  <span data-ttu-id="c2dd4-114">Uma ordem de variável personalizada pode ser especificada na operação @"microsoft.quantum.synthesis.applypermutationusingdecompositionwithvariableorder" .</span><span class="sxs-lookup"><span data-stu-id="c2dd4-114">A custom variable order can be specified in the operation @"microsoft.quantum.synthesis.applypermutationusingdecompositionwithvariableorder".</span></span>

## <a name="input"></a><span data-ttu-id="c2dd4-115">Entrada</span><span class="sxs-lookup"><span data-stu-id="c2dd4-115">Input</span></span>

### <a name="perm--int"></a><span data-ttu-id="c2dd4-116">Perm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="c2dd4-116">perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="c2dd4-117">Uma permutação de $2 ^ n $ elementos começando em 0.</span><span class="sxs-lookup"><span data-stu-id="c2dd4-117">A permutation of $2^n$ elements starting from 0.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="c2dd4-118">qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="c2dd4-118">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="c2dd4-119">Uma lista de $n $ qubits à qual a permutação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="c2dd4-119">A list of $n$ qubits to which the permutation is applied to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c2dd4-120">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c2dd4-120">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="c2dd4-121">Referências</span><span class="sxs-lookup"><span data-stu-id="c2dd4-121">References</span></span>

- [<span data-ttu-id="c2dd4-122">*Alexis de vos* , *Yvan Van Rentergem* , avçd. in Math. de comm. 2 (2), 2008, pp. 183--200</span><span class="sxs-lookup"><span data-stu-id="c2dd4-122">*Alexis De Vos* , *Yvan Van Rentergem* , Adv. in Math. of Comm. 2(2), 2008, pp. 183--200</span></span>](http://www.aimsciences.org/article/doi/10.3934/amc.2008.2.183)
- [<span data-ttu-id="c2dd4-123">*Mathias Soeken* , *Laura Tague* , *Gerhard W. Dueck* , *Rolf Drechsler* , diário de computação simbólica 73 (2016), pp. 1--26</span><span class="sxs-lookup"><span data-stu-id="c2dd4-123">*Mathias Soeken* , *Laura Tague* , *Gerhard W. Dueck* , *Rolf Drechsler* , Journal of Symbolic Computation 73 (2016), pp. 1--26</span></span>](https://www.sciencedirect.com/science/article/pii/S0747717115000188?via%3Dihub)

## <a name="see-also"></a><span data-ttu-id="c2dd4-124">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c2dd4-124">See Also</span></span>

- [<span data-ttu-id="c2dd4-125">Microsoft. Quantum. síntese. ApplyPermutationUsingDecompositionWithVariableOrder</span><span class="sxs-lookup"><span data-stu-id="c2dd4-125">Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecompositionWithVariableOrder</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecompositionWithVariableOrder)
- [<span data-ttu-id="c2dd4-126">Microsoft. Quantum. síntese. ApplyPermutationUsingTransformation</span><span class="sxs-lookup"><span data-stu-id="c2dd4-126">Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation)