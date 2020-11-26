---
uid: Microsoft.Quantum.Synthesis.TruthTablesFromPermutationFolder
title: Função TruthTablesFromPermutationFolder
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: TruthTablesFromPermutationFolder
qsharp.summary: Decomposition logic for a single variable index
ms.openlocfilehash: 86e112782825303805029b2f9f6cfd9d6ce9e8b6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96231017"
---
# <a name="truthtablesfrompermutationfolder-function"></a><span data-ttu-id="4842e-102">Função TruthTablesFromPermutationFolder</span><span class="sxs-lookup"><span data-stu-id="4842e-102">TruthTablesFromPermutationFolder function</span></span>

<span data-ttu-id="4842e-103">Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="4842e-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="4842e-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4842e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4842e-105">Lógica de decomposição para um único índice de variável</span><span class="sxs-lookup"><span data-stu-id="4842e-105">Decomposition logic for a single variable index</span></span>

```qsharp
function TruthTablesFromPermutationFolder (numVars : Int, state : Microsoft.Quantum.Synthesis.DecompositionState, index : Int) : Microsoft.Quantum.Synthesis.DecompositionState
```


## <a name="description"></a><span data-ttu-id="4842e-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="4842e-106">Description</span></span>

<span data-ttu-id="4842e-107">Isso usa o estado atual e gera uma permuta atualizada e, possivelmente, adiciona novas funções para Gates controladas.</span><span class="sxs-lookup"><span data-stu-id="4842e-107">This takes the current state and generates an updated permutation and possibly adds new functions for controlled gates.</span></span>

## <a name="input"></a><span data-ttu-id="4842e-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="4842e-108">Input</span></span>

### <a name="numvars--int"></a><span data-ttu-id="4842e-109">numVars: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4842e-109">numVars : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="state--decompositionstate"></a><span data-ttu-id="4842e-110">Estado: [decomposiçãostate](xref:Microsoft.Quantum.Synthesis.DecompositionState)</span><span class="sxs-lookup"><span data-stu-id="4842e-110">state : [DecompositionState](xref:Microsoft.Quantum.Synthesis.DecompositionState)</span></span>




### <a name="index--int"></a><span data-ttu-id="4842e-111">índice: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4842e-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--decompositionstate"></a><span data-ttu-id="4842e-112">Saída: [decomposiçãostate](xref:Microsoft.Quantum.Synthesis.DecompositionState)</span><span class="sxs-lookup"><span data-stu-id="4842e-112">Output : [DecompositionState](xref:Microsoft.Quantum.Synthesis.DecompositionState)</span></span>

