---
uid: Microsoft.Quantum.Logical.LessThanOrEqualD
title: Função LessThanOrEqualD
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanOrEqualD
qsharp.summary: Returns true if and only if a number is less than or equal to another number.
ms.openlocfilehash: 3f4ccb0888e7df7c43ff73be8a3140e3fa84d4dc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197629"
---
# <a name="lessthanorequald-function"></a><span data-ttu-id="90f6b-102">Função LessThanOrEqualD</span><span class="sxs-lookup"><span data-stu-id="90f6b-102">LessThanOrEqualD function</span></span>

<span data-ttu-id="90f6b-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="90f6b-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="90f6b-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="90f6b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="90f6b-105">Retornará true se e somente se um número for menor ou igual a outro número.</span><span class="sxs-lookup"><span data-stu-id="90f6b-105">Returns true if and only if a number is less than or equal to another number.</span></span>

```qsharp
function LessThanOrEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="90f6b-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="90f6b-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="90f6b-107">r: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="90f6b-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="90f6b-108">O primeiro valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="90f6b-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="90f6b-109">b: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="90f6b-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="90f6b-110">O segundo valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="90f6b-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="90f6b-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="90f6b-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="90f6b-112">`true` se e somente se `a` for menor ou igual a `b` .</span><span class="sxs-lookup"><span data-stu-id="90f6b-112">`true` if and only if `a` is less than or equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="90f6b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="90f6b-113">Remarks</span></span>

<span data-ttu-id="90f6b-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="90f6b-114">The following are equivalent:</span></span>

```Q#
let cond = a <= b;
let cond = LessThanOrEqualD(a, b);
```