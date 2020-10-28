---
uid: Microsoft.Quantum.Logical.GreaterThanI
title: Função GreaterThanI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanI
qsharp.summary: Returns true if and only if a number is greater than another number.
ms.openlocfilehash: ffd00d8086654a2d783a351fe254fb2ee35b9184
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693124"
---
# <a name="greaterthani-function"></a><span data-ttu-id="24a97-102">Função GreaterThanI</span><span class="sxs-lookup"><span data-stu-id="24a97-102">GreaterThanI function</span></span>

<span data-ttu-id="24a97-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="24a97-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="24a97-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="24a97-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="24a97-105">Retorna true se e somente se um número for maior que outro número.</span><span class="sxs-lookup"><span data-stu-id="24a97-105">Returns true if and only if a number is greater than another number.</span></span>

```qsharp
function GreaterThanI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="24a97-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="24a97-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="24a97-107">r: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="24a97-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="24a97-108">O primeiro valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="24a97-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="24a97-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="24a97-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="24a97-110">O segundo valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="24a97-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="24a97-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="24a97-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="24a97-112">`true` se e somente se `a` for estritamente maior que `b` .</span><span class="sxs-lookup"><span data-stu-id="24a97-112">`true` if and only if `a` is strictly greater than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="24a97-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="24a97-113">Remarks</span></span>

<span data-ttu-id="24a97-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="24a97-114">The following are equivalent:</span></span>

```Q#
let cond = a > b;
let cond = GreaterThanI(a, b);
```