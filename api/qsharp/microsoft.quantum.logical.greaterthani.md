---
uid: Microsoft.Quantum.Logical.GreaterThanI
title: Função GreaterThanI
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanI
qsharp.summary: Returns true if and only if a number is greater than another number.
ms.openlocfilehash: 06cae04150f9f0164b06a4e3d4bb78242b41dc0b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197985"
---
# <a name="greaterthani-function"></a><span data-ttu-id="210d3-102">Função GreaterThanI</span><span class="sxs-lookup"><span data-stu-id="210d3-102">GreaterThanI function</span></span>

<span data-ttu-id="210d3-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="210d3-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="210d3-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="210d3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="210d3-105">Retorna true se e somente se um número for maior que outro número.</span><span class="sxs-lookup"><span data-stu-id="210d3-105">Returns true if and only if a number is greater than another number.</span></span>

```qsharp
function GreaterThanI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="210d3-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="210d3-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="210d3-107">r: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="210d3-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="210d3-108">O primeiro valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="210d3-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="210d3-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="210d3-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="210d3-110">O segundo valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="210d3-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="210d3-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="210d3-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="210d3-112">`true` se e somente se `a` for estritamente maior que `b` .</span><span class="sxs-lookup"><span data-stu-id="210d3-112">`true` if and only if `a` is strictly greater than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="210d3-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="210d3-113">Remarks</span></span>

<span data-ttu-id="210d3-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="210d3-114">The following are equivalent:</span></span>

```Q#
let cond = a > b;
let cond = GreaterThanI(a, b);
```