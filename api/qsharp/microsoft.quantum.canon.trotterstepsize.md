---
uid: Microsoft.Quantum.Canon.TrotterStepSize
title: Função TrotterStepSize
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterStepSize
qsharp.summary: Computes Trotter step size in recursive implementation of Trotter simulation algorithm.
ms.openlocfilehash: aa5b63e058e1ea726b0d4c6eca73078831daaf3b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204684"
---
# <a name="trotterstepsize-function"></a><span data-ttu-id="20a4f-102">Função TrotterStepSize</span><span class="sxs-lookup"><span data-stu-id="20a4f-102">TrotterStepSize function</span></span>

<span data-ttu-id="20a4f-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="20a4f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="20a4f-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="20a4f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="20a4f-105">Computa o tamanho da etapa Trotter na implementação recursiva do algoritmo de simulação de Trotter.</span><span class="sxs-lookup"><span data-stu-id="20a4f-105">Computes Trotter step size in recursive implementation of Trotter simulation algorithm.</span></span>

```qsharp
function TrotterStepSize (order : Int) : Double
```


## <a name="input"></a><span data-ttu-id="20a4f-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="20a4f-106">Input</span></span>

### <a name="order--int"></a><span data-ttu-id="20a4f-107">ordem: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="20a4f-107">order : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--double"></a><span data-ttu-id="20a4f-108">Saída: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="20a4f-108">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="20a4f-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="20a4f-109">Remarks</span></span>

<span data-ttu-id="20a4f-110">Esta operação usa uma Convenção de indexação diferente da [Quant-pH/0508139](https://arxiv.org/abs/quant-ph/0508139).</span><span class="sxs-lookup"><span data-stu-id="20a4f-110">This operation uses a different indexing convention than that of [quant-ph/0508139](https://arxiv.org/abs/quant-ph/0508139).</span></span> <span data-ttu-id="20a4f-111">Em particular, `DecomposedIntoTimeStepsCA(_, 4)` corresponde ao escalar $p _2 (\lambda) $ em Quant-pH/0508139.</span><span class="sxs-lookup"><span data-stu-id="20a4f-111">In particular, `DecomposedIntoTimeStepsCA(_, 4)` corresponds to the scalar $p_2(\lambda)$ in quant-ph/0508139.</span></span>