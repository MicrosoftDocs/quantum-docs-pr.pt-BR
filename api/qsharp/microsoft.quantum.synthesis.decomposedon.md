---
uid: Microsoft.Quantum.Synthesis.DecomposedOn
title: Função decompostay
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecomposedOn
qsharp.summary: Decomposes a permutation on a variable
ms.openlocfilehash: b033723a50fb85e77c9d4baec1f94231327e9b25
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92697054"
---
# <a name="decomposedon-function"></a><span data-ttu-id="6b412-102">Função decompostay</span><span class="sxs-lookup"><span data-stu-id="6b412-102">DecomposedOn function</span></span>

<span data-ttu-id="6b412-103">Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="6b412-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="6b412-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6b412-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6b412-105">Redação de uma permutação em uma variável</span><span class="sxs-lookup"><span data-stu-id="6b412-105">Decomposes a permutation on a variable</span></span>

```qsharp
function DecomposedOn (perm : Int[], index : Int) : ((Int[], Int[]), Int[])
```


## <a name="description"></a><span data-ttu-id="6b412-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="6b412-106">Description</span></span>

<span data-ttu-id="6b412-107">Dada uma permutação $ \pi $ ( `perm` ) e um índice $i $ ( `index` ), esse método retorna três permutas $ ((\ pi_l, \ pi_r), \pi ') $ de forma que as imagens de $ \ pi_l $ e $ \ pi_r $ não alterem bits em seus elementos em índices diferentes de $i $ e imagens de $ \pi ' $ não altere o bit $i $ em seus elementos.</span><span class="sxs-lookup"><span data-stu-id="6b412-107">Given a permutation $\pi$ (`perm`) and an index $i$ (`index`), this method returns three permutations $((\pi_l, \pi_r), \pi')$ such that the images of $\pi_l$ and $\pi_r$ do not change bits in their elements at indexes other than $i$ and images of $\pi'$ do not change bit $i$ in their elements.</span></span>

## <a name="input"></a><span data-ttu-id="6b412-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="6b412-108">Input</span></span>

### <a name="perm--int"></a><span data-ttu-id="6b412-109">Perm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="6b412-109">perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="index--int"></a><span data-ttu-id="6b412-110">índice: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6b412-110">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--intintint"></a><span data-ttu-id="6b412-111">Saída: (([int](xref:microsoft.quantum.lang-ref.int)[],[int](xref:microsoft.quantum.lang-ref.int)[]),[int](xref:microsoft.quantum.lang-ref.int)[])</span><span class="sxs-lookup"><span data-stu-id="6b412-111">Output : (([Int](xref:microsoft.quantum.lang-ref.int)[],[Int](xref:microsoft.quantum.lang-ref.int)[]),[Int](xref:microsoft.quantum.lang-ref.int)[])</span></span>

