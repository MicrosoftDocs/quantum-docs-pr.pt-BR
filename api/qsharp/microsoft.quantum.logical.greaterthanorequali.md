---
uid: Microsoft.Quantum.Logical.GreaterThanOrEqualI
title: Função GreaterThanOrEqualI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanOrEqualI
qsharp.summary: Returns true if and only if a number is greater than or equal to another number.
ms.openlocfilehash: c1a513500c8a70bd7628976974387cba48162e80
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849178"
---
# <a name="greaterthanorequali-function"></a><span data-ttu-id="a9e83-102">Função GreaterThanOrEqualI</span><span class="sxs-lookup"><span data-stu-id="a9e83-102">GreaterThanOrEqualI function</span></span>

<span data-ttu-id="a9e83-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="a9e83-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="a9e83-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a9e83-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a9e83-105">Retorna true se e somente se um número for maior ou igual a outro número.</span><span class="sxs-lookup"><span data-stu-id="a9e83-105">Returns true if and only if a number is greater than or equal to another number.</span></span>

```qsharp
function GreaterThanOrEqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="a9e83-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="a9e83-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="a9e83-107">r: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a9e83-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a9e83-108">O primeiro valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="a9e83-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="a9e83-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a9e83-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a9e83-110">O segundo valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="a9e83-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="a9e83-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a9e83-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a9e83-112">`true` se e somente se `a` for maior que ou for igual a `b` .</span><span class="sxs-lookup"><span data-stu-id="a9e83-112">`true` if and only if `a` is greater than or is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9e83-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9e83-113">Remarks</span></span>

<span data-ttu-id="a9e83-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="a9e83-114">The following are equivalent:</span></span>

```qsharp
let cond = a >= b;
let cond = GreaterThanOrEqualI(a, b);
```