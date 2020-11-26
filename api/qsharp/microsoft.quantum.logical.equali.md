---
uid: Microsoft.Quantum.Logical.EqualI
title: Função equali
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualI
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: be92ef2b63981094e1a95c38e02de95c3c2bbf3a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198156"
---
# <a name="equali-function"></a><span data-ttu-id="ed716-102">Função equali</span><span class="sxs-lookup"><span data-stu-id="ed716-102">EqualI function</span></span>

<span data-ttu-id="ed716-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="ed716-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="ed716-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ed716-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ed716-105">Retorna true se e somente se duas entradas forem iguais.</span><span class="sxs-lookup"><span data-stu-id="ed716-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="ed716-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="ed716-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="ed716-107">r: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ed716-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ed716-108">O primeiro valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="ed716-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="ed716-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ed716-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ed716-110">O segundo valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="ed716-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="ed716-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="ed716-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="ed716-112">`true` se e somente se `a` for igual a `b` .</span><span class="sxs-lookup"><span data-stu-id="ed716-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed716-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed716-113">Remarks</span></span>

<span data-ttu-id="ed716-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="ed716-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualI(a, b);
```