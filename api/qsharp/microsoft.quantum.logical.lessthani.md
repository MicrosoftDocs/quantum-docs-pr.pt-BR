---
uid: Microsoft.Quantum.Logical.LessThanI
title: Função LessThanI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanI
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: 204e62a87d2b3d0070946985030d038ead686457
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696806"
---
# <a name="lessthani-function"></a><span data-ttu-id="21aee-102">Função LessThanI</span><span class="sxs-lookup"><span data-stu-id="21aee-102">LessThanI function</span></span>

<span data-ttu-id="21aee-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="21aee-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="21aee-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="21aee-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="21aee-105">Retorna true se e somente se um número for menor que outro número.</span><span class="sxs-lookup"><span data-stu-id="21aee-105">Returns true if and only if a number is less than another number.</span></span>

```qsharp
function LessThanI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="21aee-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="21aee-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="21aee-107">r: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="21aee-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="21aee-108">O primeiro valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="21aee-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="21aee-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="21aee-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="21aee-110">O segundo valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="21aee-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="21aee-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="21aee-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="21aee-112">`true` se e somente se `a` for estritamente menor que `b` .</span><span class="sxs-lookup"><span data-stu-id="21aee-112">`true` if and only if `a` is strictly less than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="21aee-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="21aee-113">Remarks</span></span>

<span data-ttu-id="21aee-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="21aee-114">The following are equivalent:</span></span>

```Q#
let cond = a < b;
let cond = LessThanI(a, b);
```