---
uid: Microsoft.Quantum.Synthesis.DecompositionState
title: Tipo definido pelo usuário de decomposiçãostate
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecompositionState
qsharp.summary: State during decomposition based on variable indexes
ms.openlocfilehash: 0547c04828a80b4f696cc17e13c8cc57d0379f96
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92697053"
---
# <a name="decompositionstate-user-defined-type"></a><span data-ttu-id="d91a3-102">Tipo definido pelo usuário de decomposiçãostate</span><span class="sxs-lookup"><span data-stu-id="d91a3-102">DecompositionState user defined type</span></span>

<span data-ttu-id="d91a3-103">Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="d91a3-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="d91a3-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d91a3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d91a3-105">Estado durante a decomposição com base em índices de variáveis</span><span class="sxs-lookup"><span data-stu-id="d91a3-105">State during decomposition based on variable indexes</span></span>

```qsharp

newtype DecompositionState = (Perm : Int[], Lfunctions : (BigInt, Int)[], Rfunctions : (BigInt, Int)[]);
```



## <a name="named-items"></a><span data-ttu-id="d91a3-106">Itens nomeados</span><span class="sxs-lookup"><span data-stu-id="d91a3-106">Named Items</span></span>

### <a name="perm--int"></a><span data-ttu-id="d91a3-107">Perm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="d91a3-107">Perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>


### <a name="lfunctions--bigintint"></a><span data-ttu-id="d91a3-108">Lfunctions: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="d91a3-108">Lfunctions : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>


### <a name="rfunctions--bigintint"></a><span data-ttu-id="d91a3-109">Rfunctions: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="d91a3-109">Rfunctions : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>



## <a name="description"></a><span data-ttu-id="d91a3-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="d91a3-110">Description</span></span>

<span data-ttu-id="d91a3-111">O estado mantém a permuta atual e as funções atualmente geradas para Gates controladas à esquerda e Gates controladas à direita.</span><span class="sxs-lookup"><span data-stu-id="d91a3-111">The state holds the current permutation and the currently generated functions for controlled gates on the left, and controlled gates on the right.</span></span>