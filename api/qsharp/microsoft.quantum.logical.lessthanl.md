---
uid: Microsoft.Quantum.Logical.LessThanL
title: Função LessThanL
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanL
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: fde57bcd9960056461bddac54300c298def8f7d5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693120"
---
# <a name="lessthanl-function"></a><span data-ttu-id="06bd5-102">Função LessThanL</span><span class="sxs-lookup"><span data-stu-id="06bd5-102">LessThanL function</span></span>

<span data-ttu-id="06bd5-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="06bd5-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="06bd5-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="06bd5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="06bd5-105">Retorna true se e somente se um número for menor que outro número.</span><span class="sxs-lookup"><span data-stu-id="06bd5-105">Returns true if and only if a number is less than another number.</span></span>

```qsharp
function LessThanL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="06bd5-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="06bd5-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="06bd5-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="06bd5-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="06bd5-108">O primeiro valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="06bd5-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="06bd5-109">b: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="06bd5-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="06bd5-110">O segundo valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="06bd5-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="06bd5-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="06bd5-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="06bd5-112">`true` se e somente se `a` for estritamente menor que `b` .</span><span class="sxs-lookup"><span data-stu-id="06bd5-112">`true` if and only if `a` is strictly less than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="06bd5-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="06bd5-113">Remarks</span></span>

<span data-ttu-id="06bd5-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="06bd5-114">The following are equivalent:</span></span>

```Q#
let cond = a < b;
let cond = LessThanL(a, b);
```