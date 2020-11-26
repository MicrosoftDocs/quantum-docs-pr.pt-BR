---
uid: Microsoft.Quantum.Logical.GreaterThanOrEqualI
title: Função GreaterThanOrEqualI
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanOrEqualI
qsharp.summary: Returns true if and only if a number is greater than or equal to another number.
ms.openlocfilehash: 0435aae4a824bd19d972e9f6b331260bbe21f692
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197782"
---
# <a name="greaterthanorequali-function"></a><span data-ttu-id="f0e1a-102">Função GreaterThanOrEqualI</span><span class="sxs-lookup"><span data-stu-id="f0e1a-102">GreaterThanOrEqualI function</span></span>

<span data-ttu-id="f0e1a-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="f0e1a-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="f0e1a-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f0e1a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f0e1a-105">Retorna true se e somente se um número for maior ou igual a outro número.</span><span class="sxs-lookup"><span data-stu-id="f0e1a-105">Returns true if and only if a number is greater than or equal to another number.</span></span>

```qsharp
function GreaterThanOrEqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="f0e1a-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="f0e1a-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="f0e1a-107">r: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f0e1a-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f0e1a-108">O primeiro valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="f0e1a-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="f0e1a-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f0e1a-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f0e1a-110">O segundo valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="f0e1a-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="f0e1a-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f0e1a-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f0e1a-112">`true` se e somente se `a` for maior que ou for igual a `b` .</span><span class="sxs-lookup"><span data-stu-id="f0e1a-112">`true` if and only if `a` is greater than or is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0e1a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0e1a-113">Remarks</span></span>

<span data-ttu-id="f0e1a-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="f0e1a-114">The following are equivalent:</span></span>

```Q#
let cond = a >= b;
let cond = GreaterThanOrEqualI(a, b);
```