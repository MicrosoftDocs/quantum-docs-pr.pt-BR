---
uid: Microsoft.Quantum.Logical.GreaterThanI
title: Função GreaterThanI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanI
qsharp.summary: Returns true if and only if a number is greater than another number.
ms.openlocfilehash: 86fc8e927c292a2ea814ed80a33de42bffdb96b1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98815949"
---
# <a name="greaterthani-function"></a><span data-ttu-id="4f5d4-102">Função GreaterThanI</span><span class="sxs-lookup"><span data-stu-id="4f5d4-102">GreaterThanI function</span></span>

<span data-ttu-id="4f5d4-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="4f5d4-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="4f5d4-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4f5d4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4f5d4-105">Retorna true se e somente se um número for maior que outro número.</span><span class="sxs-lookup"><span data-stu-id="4f5d4-105">Returns true if and only if a number is greater than another number.</span></span>

```qsharp
function GreaterThanI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="4f5d4-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="4f5d4-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="4f5d4-107">r: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4f5d4-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4f5d4-108">O primeiro valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="4f5d4-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="4f5d4-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4f5d4-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4f5d4-110">O segundo valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="4f5d4-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="4f5d4-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="4f5d4-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="4f5d4-112">`true` se e somente se `a` for estritamente maior que `b` .</span><span class="sxs-lookup"><span data-stu-id="4f5d4-112">`true` if and only if `a` is strictly greater than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f5d4-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f5d4-113">Remarks</span></span>

<span data-ttu-id="4f5d4-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="4f5d4-114">The following are equivalent:</span></span>

```qsharp
let cond = a > b;
let cond = GreaterThanI(a, b);
```