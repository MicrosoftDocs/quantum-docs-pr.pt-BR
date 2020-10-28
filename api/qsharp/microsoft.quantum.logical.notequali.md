---
uid: Microsoft.Quantum.Logical.NotEqualI
title: Função não Iguali
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualI
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 68e0e105a6b3742ec11e80ff92c39578a786aa85
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693102"
---
# <a name="notequali-function"></a><span data-ttu-id="a5527-102">Função não Iguali</span><span class="sxs-lookup"><span data-stu-id="a5527-102">NotEqualI function</span></span>

<span data-ttu-id="a5527-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="a5527-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="a5527-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a5527-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a5527-105">Retorna true se e somente se duas entradas não forem iguais.</span><span class="sxs-lookup"><span data-stu-id="a5527-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="a5527-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="a5527-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="a5527-107">r: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a5527-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a5527-108">O primeiro valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="a5527-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="a5527-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a5527-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a5527-110">O segundo valor a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="a5527-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="a5527-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a5527-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a5527-112">`true` se e somente se `a` não for igual a `b` .</span><span class="sxs-lookup"><span data-stu-id="a5527-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5527-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5527-113">Remarks</span></span>

<span data-ttu-id="a5527-114">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="a5527-114">The following are equivalent:</span></span>

```Q#
let cond = a != b;
let cond = NotEqualI(a, b);
```