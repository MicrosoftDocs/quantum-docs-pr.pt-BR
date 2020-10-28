---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecompositionWithVariableOrder
title: Operação ApplyPermutationUsingDecompositionWithVariableOrder
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingDecompositionWithVariableOrder
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.
ms.openlocfilehash: 1edbc0a2948fdf3ae67f14b3c552676feaa7f498
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92697065"
---
# <a name="applypermutationusingdecompositionwithvariableorder-operation"></a><span data-ttu-id="3484b-102">Operação ApplyPermutationUsingDecompositionWithVariableOrder</span><span class="sxs-lookup"><span data-stu-id="3484b-102">ApplyPermutationUsingDecompositionWithVariableOrder operation</span></span>

<span data-ttu-id="3484b-103">Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="3484b-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="3484b-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3484b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3484b-105">Permuta as amplitudes em um estado Quantum, considerando uma permuta usando a síntese baseada em decomposição.</span><span class="sxs-lookup"><span data-stu-id="3484b-105">Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.</span></span>

```qsharp
operation ApplyPermutationUsingDecompositionWithVariableOrder (perm : Int[], variableOrder : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="3484b-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="3484b-106">Description</span></span>

<span data-ttu-id="3484b-107">Esta operação é uma versão mais geral do @"microsoft.quantum.synthesis.applypermutationusingdecomposition" na qual a ordem variável pode ser especificada.</span><span class="sxs-lookup"><span data-stu-id="3484b-107">This operation is a more general version of @"microsoft.quantum.synthesis.applypermutationusingdecomposition" in which the variable order can be specified.</span></span> <span data-ttu-id="3484b-108">Uma ordem variável diferente altera a sequência de decomposição e as tabelas da verdade usadas para as @"microsoft.quantum.intrinsic.x" Gates controladas.</span><span class="sxs-lookup"><span data-stu-id="3484b-108">A different variable order changes the decomposition sequence and the truth tables used for the controlled @"microsoft.quantum.intrinsic.x" gates.</span></span>  <span data-ttu-id="3484b-109">Portanto, alterar a ordem da variável altera o número de Gates gerais usadas para concretizar a permutação.</span><span class="sxs-lookup"><span data-stu-id="3484b-109">Therefore, changing the variable order changes the number of overall gates used to realize the permutation.</span></span>

## <a name="input"></a><span data-ttu-id="3484b-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="3484b-110">Input</span></span>

### <a name="perm--int"></a><span data-ttu-id="3484b-111">Perm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="3484b-111">perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="3484b-112">Uma permutação de $2 ^ n $ elementos começando em 0.</span><span class="sxs-lookup"><span data-stu-id="3484b-112">A permutation of $2^n$ elements starting from 0.</span></span>


### <a name="variableorder--int"></a><span data-ttu-id="3484b-113">variableOrder: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="3484b-113">variableOrder : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="3484b-114">Uma permutação de elementos $n $ começando em 0.</span><span class="sxs-lookup"><span data-stu-id="3484b-114">A permutation of $n$ elements starting from 0.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="3484b-115">qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="3484b-115">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="3484b-116">Uma lista de $n $ qubits à qual a permutação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="3484b-116">A list of $n$ qubits to which the permutation is applied to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3484b-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3484b-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="3484b-118">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="3484b-118">See Also</span></span>

- [<span data-ttu-id="3484b-119">Microsoft. Quantum. síntese. ApplyPermutationUsingDecomposition</span><span class="sxs-lookup"><span data-stu-id="3484b-119">Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition)
- [<span data-ttu-id="3484b-120">Microsoft. Quantum. síntese. ApplyPermutationUsingTransformation</span><span class="sxs-lookup"><span data-stu-id="3484b-120">Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation)