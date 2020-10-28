---
uid: Microsoft.Quantum.Logical.LessThanOrEqualI
title: Função LessThanOrEqualI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanOrEqualI
qsharp.summary: Returns true if and only if a number is less than or equal to another number.
ms.openlocfilehash: dd934fde3fae9c1a43032b4b08ac03afa72798d1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693117"
---
# <a name="lessthanorequali-function"></a><span data-ttu-id="a3b12-102">Função LessThanOrEqualI</span><span class="sxs-lookup"><span data-stu-id="a3b12-102">LessThanOrEqualI function</span></span>

<span data-ttu-id="a3b12-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="a3b12-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="a3b12-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a3b12-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a3b12-105">Retornará true se e somente se um número for menor ou igual a outro número.</span><span class="sxs-lookup"><span data-stu-id="a3b12-105">Returns true if and only if a number is less than or equal to another number.</span></span>

```qsharp
function LessThanOrEqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="a3b12-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="a3b12-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="a3b12-107">r: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a3b12-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a3b12-108">O primeiro valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="a3b12-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="a3b12-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a3b12-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a3b12-110">O segundo valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="a3b12-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="a3b12-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a3b12-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a3b12-112">`true` se e somente se `a` for menor ou igual a `b` .</span><span class="sxs-lookup"><span data-stu-id="a3b12-112">`true` if and only if `a` is less than or equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3b12-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a3b12-113">Remarks</span></span>

<span data-ttu-id="a3b12-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="a3b12-114">The following are equivalent:</span></span>

```Q#
let cond = a <= b;
let cond = LessThanOrEqualI(a, b);
```