---
uid: Microsoft.Quantum.Logical.LessThanOrEqualI
title: Função LessThanOrEqualI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanOrEqualI
qsharp.summary: Returns true if and only if a number is less than or equal to another number.
ms.openlocfilehash: 9438fc05b4ccb041b087f9cfeb30ac0c8cfcabd6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98815616"
---
# <a name="lessthanorequali-function"></a><span data-ttu-id="6421f-102">Função LessThanOrEqualI</span><span class="sxs-lookup"><span data-stu-id="6421f-102">LessThanOrEqualI function</span></span>

<span data-ttu-id="6421f-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="6421f-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="6421f-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6421f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6421f-105">Retornará true se e somente se um número for menor ou igual a outro número.</span><span class="sxs-lookup"><span data-stu-id="6421f-105">Returns true if and only if a number is less than or equal to another number.</span></span>

```qsharp
function LessThanOrEqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="6421f-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="6421f-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="6421f-107">r: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6421f-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6421f-108">O primeiro valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="6421f-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="6421f-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6421f-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6421f-110">O segundo valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="6421f-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="6421f-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="6421f-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="6421f-112">`true` se e somente se `a` for menor ou igual a `b` .</span><span class="sxs-lookup"><span data-stu-id="6421f-112">`true` if and only if `a` is less than or equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="6421f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6421f-113">Remarks</span></span>

<span data-ttu-id="6421f-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="6421f-114">The following are equivalent:</span></span>

```qsharp
let cond = a <= b;
let cond = LessThanOrEqualI(a, b);
```